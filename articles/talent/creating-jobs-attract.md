---
title: Vytvoření práce v aplikaci Attract
description: Toto téma popisuje prvky pracovního místa v aplikaci Attract. Také vysvětluje, jakým způsobem vytvořit pracovní místo.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 95bc75596f6f014b58160022f41ae86a825c5afc
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527259"
---
# <a name="create-a-job-in-attract"></a>Vytvoření práce v aplikaci Attract

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje prvky pracovního místa v aplikaci Microsoft Dynamics 365 Talent: Attract. Také vysvětluje, jakým způsobem vytvořit pracovní místo.

## <a name="job-creation"></a>Vytvoření práce

Správci, náboroví pracovníci a náboroví manažeři mohou vytvářet pracovní místa. Při vytváření pracovního místa budete vyzváni k výběru vaší role v procesu: správce náboru nebo náborář. Po výběru role budete vyzváni k výběru šablony procesu. Vyberete-li možnost **Přeskočit**, je použita výchozí šablona. Další informace o šablonách procesu naleznete v tématu [Vytvoření šablony procesu v aplikaci Attract](./process-templates-attract.md).

Pracovní místo v aplikaci Attract obsahuje podrobnosti o pracovním místě, náborovém týmu, procesu náboru, zveřejnění pracovních míst a analytiku.

## <a name="job-details"></a>Podrobnosti o práci

Karta **Detaily pracovního místa** obsahuje podrobnosti o odpovědnostech a atributech pracovního místa. Pole pro název pracovního místa, popis pracovního místa a lokalitu jsou povinná. Ostatní pole jsou volitelná.

Ve výchozím nastavení je v poli **Počet volných míst** zadána hodnota **1**. Hodnotu však lze upravit. Jakmile je připravena nabídka pracovního místa, hodnota v poli **Počet volných míst** se postupně snižuje.

Pokud je v centru pro správu zapnutá správa pracovních míst, je k dispozici vyhledávací hodnota **Aktualizovat pracovní místa**. Tento vyhledávací kód čte entitu JobPosition v aplikaci Common Data Service a vrací seznam pozic, které lze pro pracovní místo vybrat. Pokud počet pozic, které vyberete, přesáhne počet otevřených pozic, zobrazí se upozornění. Je-li pozice použita ve více pracovních místech, zobrazí se varování.

> [!NOTE]
> Správa pozice je k dispozici s doplňkem Comprehensive Hiring.

V závislosti na nastavení v aktivitě nabídky procesu náboru lze číslo pozice v nabídce použít dvakrát. Další informace naleznete v tématu [Aktivity v procesech náboru](./activities-attract.md).

Aplikace Attract obsahuje výchozí sadu **dovedností**. Tyto dovednosti se při psaní zobrazují jako návrhy. Můžete přidat více dovedností tak, že zadáte do tohoto pole text nové dovednosti a pak stisknete klávesu Enter.

Aplikace Attract obsahuje výchozí sadu **pracovních funkcí**. Můžete přidat až tři další pracovní funkce tak, že zadáte do tohoto pole novou pracovní funkci a pak stiskněte klávesu Enter.

Aplikace Attract obsahuje výchozí sadu **podnikových odvětví**. Můžete přidat až tři další podniková odvětví, že zadáte do tohoto pole nové podnikové odvětví a pak stiskněte klávesu Enter.

## <a name="hiring-team"></a>Náborový tým

Na kartě **Náborový tým** je uveden seznam osob, kterých se bude tato práce týkat. Při přidání uživatelů do náborového týmu jim musí být přiřazena role náborového týmu. Role určuje data, ke kterým uživatelé mají přístup, a upozornění, která obdrží. Lze vybírat tyto role: **Náborář**, **Manažer náboru**, **Delegovat** a **Vedoucí pohovoru**. Další informace o oprávněních rolí naleznete v dokumentu "Správa rolí". Náboráři a manažeři náboru mohou jmenovat jednoho nebo více delegátů, kteří budou jednat jejich jménem. Další informace o delegátech naleznete v tématu [Zabezpečení a správa rolí v aplikaci Attract](./security-attract.md).

Po aktivaci pracovního místu lze náborový tým aktualizovat.

## <a name="process"></a>Zpracovat

Výchozí informace týkající se procesu náboru jsou založeny na šabloně procesu, která byla vybrána při vytvoření pracovního místa. Pokud v té době nebyla vybrána konkrétní šablona, použije se výchozí šablona. Při definování procesu náboru můžete přidat nebo odebrat různé fáze, s výjimkou fáze Potenciální zákazník, žádost a Nabídka. Ačkoli fázi Potenciální zákazník nelze odebrat, je možné ji vypnout. V každé fázi lze přidat nebo odebrat jednu nebo více předdefinovaných aktivit.

Další informace o aktivitách, které lze přidat do procesu náboru, naleznete v tématu [Aktivity v procesech náboru](./activities-attract.md).

> [!NOTE]
> Po aktivaci pracovního místu lze proces náboru aktualizovat.

## <a name="postings"></a>Zaúčtování

Po aktivaci pracovního místa je lze zveřejnit. Pracovní místa může zveřejnit jen náborář a správce. Pracovní místo lze zveřejnit na webu Talent Careers (kariérní web systému Dynamics 365 Talent) nebo LinkedIn. Tým Attract průběžně pracuje na partnerství s agregátory vývěsky volných míst. Tento seznam se bude průběžně rozšiřovat. Když je práce zveřejněna pouze jako interní, uchazeči potřebují účet AAD k zobrazení pracovní nabídky a podání žádosti. Pokud je nabídka práce uvedena jako veřejná, uchazeči mohou zobrazit nabídky a zažádat za ně pomocí všech možností ověřování. 

Další informace o nabídce pracovních míst naleznete v tématu [Nastavení kariérního webu v aplikaci Microsoft Dynamics 365 Talent - Attract](career-site.md).

> [!NOTE]
> Funkce zveřejnění nabídky volných míst je k dispozici pouze s doplňkem Comprehensive Hiring pro systém Attract.

## <a name="activate"></a>Aktivovat

Po aktivaci pracovního místa je možné ho zveřejnit a přidat do něho potenciální zákazníky a uchazeče. Možnost přidání potenciálních zákazníků do nabídky volného místa je nastaven v aktivitě Potenciální zákazník v procesu náboru.

> [!NOTE]
> Po aktivaci pracovního místu lze proces náboru aktualizovat.

## <a name="prospects-and-applicants"></a>Potenciální zákazníci a uchazeči

Možnost přidání potenciálních zákazníků do nabídky volného místa je nastavena v [Aktivity v procesech náboru](./activities-attract.md#prospect-activity) v procesu náboru. Tato možnost by měla být nastavena před aktivací pracovního místa. Po aktivaci pracovního místa do něho lze přidat potenciální zákazníky a uchazeče.

## <a name="approvals"></a>Schválení

Pracovní místa v aplikaci Attract lze odeslat ke schválení. Ne všechna pracovní místa vyžadují schválení. Požadavek je nastaven na úrovni šablony. Ve výchozím nastavení nejsou schválení v šabloně vypnutá. Pokud chcete nastavit schválení, přejděte k šabloně procesu a nastavte v poli **Schválení** výchozí hodnotu. Pak při vytvoření pracovního místa vyberte tuto šablonu.

Po uložení pracovního místa je možné ho odeslat ke schválení. V následující tabulce jsou uvedeny stavy dokumentu používající schválení.

| Stav   | Kraj                                                               |
|----------|---------------------------------------------------------------------|
| Koncept    | Pracovní pozice byla uložena, ale nebyla odeslána do workflowu. |
| Čekající  | Pracovní pozice byla předložena schvalovatelům.                            |
| Schváleno | Pracovní pozice byla schválena, ale nebyla aktivována.            |
| Zamítnuto | Pracovní pozice byla zamítnuta a nemůže být aktivována.               |
| Aktivní   | Pracovní pozice byla schválena a aktivována.                            |

V seznamu pracovních pozic můžete filtrovat stavy úloh.

Schválení lze odeslat uživateli Microsoft Azure Active Directory (Azure AD) ve společnosti. Schválení jsou odeslána současně všem uživatelům, kteří jsou uvedeni jako schvalovatelé. Všichni schvalovatelé musí schválit práci před tím, než bude možné jít dále. Pokud jeden schvalovatel práci zamítne, zobrazí se u ní stav **Odmítnuto**. Po schválení pracovního místa je lze aktivovat.

Pokud uživatel nabídku upraví po schválení, ale neaktivuje ji, bude stav práce obnoven na **Koncept** a bude nutné ji znovu odeslat ke schválení. Poté, co byla schválená práce aktivována, nelze ji upravit.

Osoby, které jsou uvedeny jako schvalovatelé, obdrží upozornění v aplikaci Attract a e-mailovou zprávu s informací, že se mají položku ke schválení.  Schvalující může v e-mailu kliknutím na odkaz práci otevřít, zkontrolovat podrobnosti a schválit ji nebo zamítnout. Po nastavení stavu práce na **Schváleno** nebo **Zamítnuto**, předkladatel bude upozorněn v systému Attract a obdrží e-mail. Schvalující také obdrží e-mailové připomenutí, pokud na žádost o schválení neodpoví do 24 hodin.

> [!NOTE]
> Můžete vytvořit vlastní e-mailové šablony ke schvalování emailů. Další informace získáte v části [Vytvoření a správa e-mailových šablon](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Vytvoření práce

Podle následujícího postupu vytvořte pracovní místo.

1. Přejděte na **Pracovní místa**.
2. Zvolte **Nové**.
3. V poli **Název práce** zadejte název práce. Do pole **Role** zadejte svou roli.
4. V poli **Šablona** vyberte šablonu. Případně vyberte možnost **Přeskočit**. Vyberete-li možnost **Přeskočit**, použije se šablona, která je označena jako výchozí.

    Pokud by měl dokument projít schvalovacím procesem, vyberte šablonu, ve kterém je pole **Schvalovací proces** nastaveno na **výchozí**.

5. Na kartě **Detaily** zadejte podrobnosti pracovního místa. Pole **Název**, **Popis práce** a **Umístění** jsou povinná.
6. Zvolte **Uložit**.
7. Na kartě **Náborový tým** přidejte manažera náboru, náboráře nebo vedoucího pohovoru.
8. Zvolte **Uložit**.
9. Na kartě **Proces** podle potřeby přidávejte nebo odebírejte fáze:

    - Chcete-li přidat fázi, vyberte **+ nová fáze**.
    - Chcete-li odebrat fázi, najeďte myší nad fázi, kterou chcete odebrat, a poté zvolte tlačítko koše, které se objeví.

        > [!NOTE]
        > Fáze Potenciální uchazeč, Žádost a Nabídka nemohou být odstraněny.

10. Podle potřeby přidejte nebo odeberte aktivity:

    - Pokud chcete přidat aktivitu, přetáhněte ji ze seznamu na pravé straně do příslušné fáze. Případně na aktivitu dvakrát klikněte a pak vyberte fázi, do které ji chcete přidat.
    - Chcete-li odstranit aktivitu, rozbalte ji a pak vyberte tlačítko koše v záhlaví aktivity.

11. Zvolte **Uložit**.
12. Pokud jste vybrali použití procesu schválení, postupujte takto:

    1. Vyberte **+ Přidat schvalovatele** a poté zadejte uživatele, který má účet Azure AD. Můžete přidat více schvalujících.
    2. Vyberte **Odeslat schvalovatelům**.

    Pole **Stav práce** v pracovní pozici je nastaveno na **čekající**. Poté, co se hodnota v poli **Stav práce** změní na **Schváleno**, lze pracovní pozici aktivovat.

13. Chcete-li pracovní pozici aktivovat, zaškrtněte políčko **Aktivovat**.
14. Pokud chcete pracovní pozici zveřejnit, přejděte na **Zveřejnit** a vyberte **Zveřejint** na webu Talent Careers nebo LinkedIn.
