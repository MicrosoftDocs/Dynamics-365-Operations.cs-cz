---
title: Koncept společnosti v Dataverse
description: Toto téma popisuje integraci dat společností mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f0e3950f2b35dd8b8dbf50601b7d6b6d624863e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683668"
---
# <a name="company-concept-in-dataverse"></a>Koncept společnosti v Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Koncept *společnosti* v Finance and Operations je právní i obchodní konstrukt. Je to také hranice pro zabezpečení a viditelnost dat. Uživatelé pracují vždy v kontextu jedné společnosti a většina dat je rozdělena podle společnosti.

Dataverse nemá ekvivalentní koncepci. Nejbližší koncept je *organizační jednotka*, která je primárně hranicí zabezpečení a viditelnosti pro uživatelská data. Tento koncept nemá stejné právní nebo obchodní důsledky jako koncepce společnosti.

Vzhledem k tomu, že organizační jednotka a společnost nejsou rovnocennými koncepty, není možné vynutit mapování mezi nimi (1:1) pro účely integrace Dataverse. Protože však uživatelé musí mít ve výchozím nastavení možnost zobrazit stejné řádky v aplikaci a Dataverse, společnost Microsoft zavedla novou entitu v aplikaci Dataverse s názvem cdm\_Company. Tato entita je ekvivalentní s entitou společnosti v aplikaci. Chcete-li zajistit, aby viditelnost řádků byla ekvivalentní mezi aplikací a Dataverse, doporučujeme následující nastavení dat v aplikaci Dataverse:

+ Pro každý řádek společnosti Finance and Operations, který je povolen pro duální zápis, je vytvořen přidružený řádek cdm\_Company.
+ Když je vytvořen řádek cdm\_Company a je povolen pro duální zápis, je vytvořena výchozí organizační jednotka se stejným názvem. Přestože je pro tuto organizační jednotku automaticky vytvořen výchozí tým, není tato organizační jednotka použita.
+ Je vytvořen samostatný tým vlastníků se stejným názvem. Je také spojen s organizační jednotkou.
+ Ve výchozím nastavení je vlastník libovolného řádku vytvořeného a dvojitě zapsaného do Dataverse nastaven na tým "DW Owner", který je propojen s přidruženou organizační jednotkou.

Následující obrázek znázorňuje příklad nastavení dat v Dataverse.

![Nastavení dat v Dataverse](media/dual-write-company-1.png)

Z důvodu této konfigurace bude každý řádek, který se týká společnosti USMF, vlastněn týmem, který je propojen s organizační jednotkou USMF v aplikaci Dataverse. Každý uživatel, který má přístup k této organizační jednotce prostřednictvím role zabezpečení nastavené na zobrazení na úrovni organizační jednotky, je tedy nyní schopen tyto řádky zobrazit. Následující příklad ukazuje, jak lze týmy použít k zajištění správného přístupu k těmto řádkům.

+ Role Manažer prodeje je přidělena členům týmu USMF Sales.
+ Uživatelé, kteří mají roli manažer prodeje, mohou přistupovat ke všem řádkům obchodních vztahů, které jsou členy stejné organizační jednotky, v níž jsou členy.
+ Tým USMF Sales je propojen s dříve uvedenou organizační jednotkou USMF.
+ Proto mohou členové týmu USMF Sales zobrazit jakýkoli obchodní vztah, který je vlastněn uživatelem USMF DW, který by pocházel z entity společnosti USMF v aplikaci Finance and Operations.

![Jak lze použít týmy](media/dual-write-company-2.png)

Jak ukazuje předchozí ilustrace, toto mapování 1:1 mezi organizační jednotkou, společností a týmem je pouze výchozím bodem. V tomto příkladu je nová obchodní jednotka Europe vytvořena ručně v aplikaci Dataverse jako nadřazená pro DEMF i ESMF. Tato nová kořenová organizační jednotka nesouvisí s dvojím zápisem. Lze ji však použít k tomu, aby členové týmu EUR Sales měli přístup k datům obchodních vztahů v DEMF i v ESMF nastavením viditelnosti dat na **Nadřazená/podřízená OJ** v přidružené roli zabezpečení.

Závěrečným tématem, které je třeba projednat, je jak dvojí zápis určuje, kterému týmu vlastníků se mají přiřadit řádky. Toto chování je řízeno polem **Výchozí vlastnící tým** v řádku cdm\_Company. Je-li pro řádek cdm\_Company povolen duální zápis, modul plug-in automaticky vytvoří přidruženou organizační jednotku a tým vlastníků (pokud již neexistuje) a nastaví pole **Výchozí vlastnící tým**. Správce může toto pole změnit na jinou hodnotu. Správce však nemůže vymazat pole, pokud je entita povolena pro duální zápis.

> [!div class="mx-imgBorder"]
![Pole výchozího vlastnícího týmu](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Prokládání a zavádění společnosti

Integrace Dataverse přináší paritu společnosti použitím identifikátoru společnosti k prokládání dat. Jak ukazuje následující ilustrace, všechny tabulky specifické pro společnost jsou rozšířeny tak, aby měly vztah N:1 s entitou cdm\_Company.

> [!div class="mx-imgBorder"]
![Vztah N:1 mezi entitou specifickou pro společnost a entitou cdm_Company](media/dual-write-bootstrapping.png)

+ U řádků se po přidání a uložení společnosti hodnota změní na jen pro čtení. Uživatelé by proto měli zajistit, aby vybrali správnou firmu.
+ Pouze řádky s daty společnosti jsou způsobilé pro duální zápis mezi aplikací a Dataverse.
+ Pro existující data Dataverse bude brzy k dispozici zaváděcí praxe vedená správcem.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Automatické vyplnění názvu společnosti v aplikacích pro zapojení zákazníků

Existuje několik způsobů, jak automaticky vyplnit název společnosti v aplikacích pro zapojení zákazníků.

+ Pokud jste správcem systému, můžete výchozí společnost nastavit přechodem na **Pokročilé nastavení > Systém > Zabezpečení > Uživatelé**. Otevřete formulář **Uživatel** a v sekci **Informace o organizaci** nastavte hodnotu **Výchozí společnost ve Forms**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Nastavení výchozí společnosti v sekci Informace o organizaci.":::

+ Pokud máte oprávnění pro **zápis** v entitě **Systémový uživatel** pro úroveň **Obchodní jednotka**, můžete výchozí společnost změnit v libovolném formuláři výběrem společnosti z rozevírací nabídky **Společnost**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Změna názvu společnosti pro nový účet.":::

+ Pokud máte oprávnění pro **zápis** v datech více než jedné společnosti, můžete výchozí společnost změnit výběrem řádku, který patří jiné společnosti.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Výběr řádku změní výchozí společnost.":::

+ Pokud jste konfigurátor nebo správce systému a chcete automaticky vyplnit data společnosti do vlastního formuláře, můžete použít [události formuláře](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Přidejte odkaz na JavaScript do **msdyn_ / DefaultCompany.js** a použijte následující události. Můžete použít jakýkoli předpřipravný formulář, například formulář **Účet**.

    + Událost **OnLoad** pro formulář: Nastavte pole **defaultCompany**.
    + Událost **OnChange** pro pole **Společnost**: Nastavte pole **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Použití filtrování na základě kontextu společnosti

Chcete-li použít filtrování na základě kontextu společnosti ve vlastních formulářích nebo ve vlastních vyhledávacích polích přidaných do standardních formulářů, otevřete formulář a použijte sekci **Filtrování souvisejících záznamů** pro použití filtru společnosti. Tohle musíte pro každé vyhledávací pole, které vyžaduje filtrování na základě nejnižší společnosti v daném řádku. Nastavení je zobrazeno pro **Účet** na následujícím obrázku.

:::image type="content" source="media/apply-company-context.png" alt-text="Použití kontextu společnosti":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]