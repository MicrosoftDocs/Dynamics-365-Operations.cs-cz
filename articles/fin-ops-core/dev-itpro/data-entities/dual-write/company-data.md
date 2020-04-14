---
title: Koncept společnosti v Common Data Service
description: Toto téma popisuje integraci dat společností mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a39cf5fa980d9a815ba675e410589dbd1279c83
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172893"
---
# <a name="company-concept-in-common-data-service"></a>Koncept společnosti v Common Data Service

[!include [banner](../../includes/banner.md)]


Koncept *společnosti* v Finance and Operations je právní i obchodní konstrukt. Je to také hranice pro zabezpečení a viditelnost dat. Uživatelé pracují vždy v kontextu jedné společnosti a většina dat je rozdělena podle společnosti.

Common Data Service nemá ekvivalentní koncepci. Nejbližší koncept je *organizační jednotka*, která je primárně hranicí zabezpečení a viditelnosti pro uživatelská data. Tento koncept nemá stejné právní nebo obchodní důsledky jako koncepce společnosti.

Vzhledem k tomu, že organizační jednotka a společnost nejsou rovnocennými koncepty, není možné vynutit mapování mezi nimi (1:1) pro účely integrace Common Data Service. Protože však uživatelé musí mít ve výchozím nastavení možnost zobrazit stejné záznamy v aplikaci a Common Data Service, společnost Microsoft zavedla novou entitu v aplikaci Common Data Service s názvem cdm\_Company. Tato entita je ekvivalentní s entitou společnosti v aplikaci. Chcete-li zajistit, aby viditelnost záznamů byla ekvivalentní mezi aplikací a Common Data Service, doporučujeme následující nastavení dat v aplikaci Common Data Service:

+ Pro každý záznam společnosti Finance and Operations, který je povolen pro duální zápis, je vytvořen přidružený záznam cdm\_Company.
+ Když je vytvořen záznam cdm\_Company a je povolen pro duální zápis, je vytvořena výchozí organizační jednotka se stejným názvem. Přestože je pro tuto organizační jednotku automaticky vytvořen výchozí tým, není tato organizační jednotka použita.
+ Je vytvořen samostatný tým vlastníků se stejným názvem. Je také spojen s organizační jednotkou.
+ Ve výchozím nastavení je vlastník libovolného záznamu vytvořeného a s dvojím zápisem do Common Data Service nastaven na tým "DW Owner", který je propojen s přidruženou organizační jednotkou.

Následující obrázek znázorňuje příklad nastavení dat v Common Data Service.

![Nastavení dat v Common Data Service](media/dual-write-company-1.png)

Z důvodu této konfigurace bude každý záznam, který se týká společnosti USMF, vlastněn týmem, který je propojen s organizační jednotkou USMF v aplikaci Common Data Service. Každý uživatel, který má přístup k této organizační jednotce prostřednictvím role zabezpečení nastavené na zobrazení na úrovni organizační jednotky, je tedy nyní schopen tyto záznamy zobrazit. Následující příklad ukazuje, jak lze týmy použít k zajištění správného přístupu k těmto záznamům.

+ Role Manažer prodeje je přidělena členům týmu USMF Sales.
+ Uživatelé, kteří mají roli manažer prodeje, mohou přistupovat ke všem záznamům obchodních vztahů, které jsou členy stejné organizační jednotky, v níž jsou členy.
+ Tým USMF Sales je propojen s dříve uvedenou organizační jednotkou USMF.
+ Proto mohou členové týmu USMF Sales zobrazit jakýkoli obchodní vztah, který je vlastněn uživatelem USMF DW, který by pocházel z entity společnosti USMF v aplikaci Finance and Operations.

![Jak lze použít týmy](media/dual-write-company-2.png)

Jak ukazuje předchozí ilustrace, toto mapování 1:1 mezi organizační jednotkou, společností a týmem je pouze výchozím bodem. V tomto příkladu je nová obchodní jednotka Europe vytvořena ručně v aplikaci Common Data Service jako nadřazená pro DEMF i ESMF. Tato nová kořenová organizační jednotka nesouvisí s dvojím zápisem. Lze ji však použít k tomu, aby členové týmu EUR Sales měli přístup k datům obchodních vztahů v DEMF i v ESMF nastavením viditelnosti dat na **Nadřazená/podřízená OJ** v přidružené roli zabezpečení.

Závěrečným tématem, které je třeba projednat, je jak dvojí zápis určuje, kterému týmu vlastníků se mají přiřadit záznamy. Toto chování je řízeno polem **Výchozí vlastnící tým** v záznamu cdm\_Company. Je-li záznam cdm\_Company povolen pro duální zápis, modul plug-in automaticky vytvoří přidruženou organizační jednotku a tým vlastníků (pokud již neexistuje) a nastaví pole **Výchozí vlastnící tým**. Správce může toto pole změnit na jinou hodnotu. Správce však nemůže vymazat pole, pokud je entita povolena pro duální zápis.

> [!div class="mx-imgBorder"]
![Pole výchozího vlastnícího týmu](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Prokládání a zavádění společnosti

Integrace Common Data Service přináší paritu společnosti použitím identifikátoru společnosti k prokládání dat. Jak ukazuje následující ilustrace, všechny entity specifické pro společnost jsou rozšířeny tak, aby měly vztah N:1 s entitou cdm\_Company.

> [!div class="mx-imgBorder"]
![Vztah N:1 mezi entitou specifickou pro společnost a entitou cdm_Company](media/dual-write-bootstrapping.png)

+ U záznamů se po přidání a uložení společnosti hodnota změní na jen pro čtení. Uživatelé by proto měli zajistit, aby vybrali správnou firmu.
+ Pouze záznamy s daty společnosti jsou způsobilé pro duální zápis mezi aplikací a Common Data Service.
+ Pro existující data Common Data Service bude brzy k dispozici zaváděcí praxe vedená správcem.
