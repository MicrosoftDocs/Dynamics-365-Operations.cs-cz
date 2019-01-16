---
title: "Vytvoření, schválení a zveřejnění pracovích míst v aplikaci Attract"
description: "Toto téma popisuje prvky pracovního místa v aplikaci Attract. Také vysvětluje, jakým způsobem vytvořit pracovní místo."
author: josaw
manager: AnnBe
ms.date: 12/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 6c5daa4050d63303f1ac10c24901e5b1182cb62b
ms.contentlocale: cs-cz
ms.lasthandoff: 12/23/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a>Vytvoření, schválení a zveřejnění pracovích míst v aplikaci Attract

[!include [banner](includes/banner.md)]

Toto téma popisuje prvky pracovního místa v aplikaci Microsoft Dynamics 365 for Talent: Attract. Také vysvětluje, jakým způsobem vytvořit pracovní místo.

## <a name="job-creation"></a>Vytvoření práce

Správci, náboroví pracovníci a náboroví manažeři mohou vytvářet pracovní místa. Při vytváření pracovního místa budete vyzváni k výběru vaší role v procesu: správce náboru nebo náborář. Po výběru role budete vyzváni k výběru šablony procesu. Vyberete-li možnost **Přeskočit**, je použita výchozí šablona. Další informace o šablonách procesu naleznete v tématu [Vytvoření šablony procesu v aplikaci Attract](./process-templates-attract.md).

Pracovní místo v aplikaci Attract obsahuje podrobnosti o pracovním místě, náborovém týmu, procesu náboru, zveřejnění pracovních míst a analytiku.

## <a name="job-details"></a>Podrobnosti o práci

Karta **Detaily pracovního místa** obsahuje podrobnosti o odpovědnostech a atributech pracovního místa. Pole pro název pracovního místa, popis pracovního místa a lokalitu jsou povinná. Ostatní pole jsou volitelná.

Ve výchozím nastavení je v poli **Počet volných míst** zadána hodnota **1**. Hodnotu však lze upravit. Jakmile je připravena nabídka pracovního místa, hodnota v poli **Počet volných míst** se postupně snižuje.

Pokud je v centru pro správu zapnutá správa pracovních míst, je k dispozici vyhledávací hodnota **Aktualizovat pracovní místa**. Tento vyhledávací kód čte entitu JobPosition v aplikaci Common Data Service pro aplikace a vrací seznam pozic, které lze pro pracovní místo vybrat. Pokud počet pozic, které vyberete, přesáhne počet otevřených pozic, zobrazí se upozornění. Je-li pozice použita ve více pracovních místech, zobrazí se varování.

> [!NOTE]
> Správa pozice je k dispozici s doplňkem Comprehensive Hiring.

V závislosti na nastavení v aktivitě nabídky procesu náboru lze číslo pozice v nabídce použít dvakrát. Další informace naleznete v tématu [Proces náboru](./activities-attract.md).

Aplikace Attract obsahuje výchozí sadu **dovedností**. Tyto dovednosti se při psaní zobrazují jako návrhy. Můžete přidat více dovedností tak, že zadáte do tohoto pole text nové dovednosti a pak stisknete klávesu Enter.

Aplikace Attract obsahuje výchozí sadu **pracovních funkcí**. Můžete přidat až tři další pracovní funkce tak, že zadáte do tohoto pole novou pracovní funkci a pak stiskněte klávesu Enter.

Aplikace Attract obsahuje výchozí sadu **podnikových odvětví**. Můžete přidat až tři další podniková odvětví, že zadáte do tohoto pole nové podnikové odvětví a pak stiskněte klávesu Enter.

## <a name="hiring-team"></a>Náborový tým

Na kartě **Náborový tým** je uveden seznam osob, kterých se bude tato práce týkat. Při přidání uživatelů do náborového týmu jim musí být přiřazena role náborového týmu. Role určuje data, ke kterým uživatelé mají přístup, a upozornění, která obdrží. Lze vybírat tyto role: **Náborář**, **Manažer náboru**, **Delegovat** a **Vedoucí pohovoru**. Další informace o oprávněních rolí naleznete v dokumentu "Správa rolí". Náboráři a manažeři náboru mohou jmenovat jednoho nebo více delegátů, kteří budou jednat jejich jménem. Další informace o delegátech naleznete v tématu [Zabezpečení a správa rolí v aplikaci Attract](./security-attract.md).

Po aktivaci pracovního místu lze náborový tým aktualizovat.

## <a name="process"></a>Zpracovat

Výchozí informace týkající se procesu náboru jsou založeny na šabloně procesu, která byla vybrána při vytvoření pracovního místa. Pokud v té době nebyla vybrána konkrétní šablona, použije se výchozí šablona. Při definování procesu náboru můžete přidat nebo odebrat různé fáze, s výjimkou fáze Potenciální zákazník, žádost a Nabídka. Ačkoli fázi Potenciální zákazník nelze odebrat, je možné ji vypnout. V každé fázi lze přidat nebo odebrat jednu nebo více předdefinovaných aktivit.

Další informace o aktivitách, které lze přidat do procesu náboru, naleznete v tématu [Aktivity náborového procesu v aplikaci Attract](./activities-attract.md).

> [!NOTE]
> Po aktivaci pracovního místu lze proces náboru aktualizovat.

## <a name="postings"></a>Zaúčtování

Po aktivaci pracovního místa je lze zveřejnit. Pracovní místa může zveřejnit jen náborář a správce. Pracovní místo lze zveřejnit na webu Talent Careers (kariérní web systému Microsoft Dynamics 365 for Talent) nebo LinkedIn. 

> [!NOTE]
> Při publikování procesu ve službě LinkedIn je důležité všimnout si tří důležitých věcí.
> 1. Pracovní nabídky publikované ve službě LinkedIn se publikují jako pracovní nabídky s omezeným výpisem. Nelze je propagovat na celém webu LinkedIn. Pokud chcete propagovat pracovní nabídky s omezeným výpisem ve službě LinkedIn z Attract, měli byste spolupracovat s LinkedIn a umožnit sbalení pracovní nabídky. Podrobnější informace získáte z následujících odkazů a může vám je poskytnout podpora společnosti LinkedIn.
>
>    [Omezené seznamy vs. prémiové nabídky volných míst ke sbalení pracovních nabídek](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [Časté otázky týkající se sbalení pracovní nabídky](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. Při publikování pracovních nabídek ve službě LinkedIn Attract předá organizaci Microsoft 365 jméno u pracovní nabídky. LinkedIn propojí volná místa se společností na straně LinkedIn na základě předaného jména organizace. Pokud je vaše nabídka na webu LinkedIn spojená se špatnou společností, ověřte, zda název organizace Microsoft 365 odpovídá názvu společnosti ve službě LinkedIn.  
>
>    [Změna kontaktní adresy a další](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    Pokud máte po dokončení tohoto kroku potíže, obraťte se na podporu LinkedIn. 
> 
> 1. Může trvat až 24 hodin, než se nabídky volných míst publikované ve službě LinkedIn zobrazí uchazečům. Důvodem je současný proces dávkového publikování volných míst službou LinkedIn.

Tým Attract průběžně pracuje na partnerství s agregátory vývěsky volných míst. Tento seznam se bude průběžně rozšiřovat.

Další informace o nabídce volných pracovních míst naleznete v tématu [Funkce Kariérní web v aplikaci Attract](./career-site.md).

> [!NOTE]
> Funkce zveřejnění nabídky volných míst je k dispozici pouze s doplňkem Comprehensive Hiring pro systém Attract.

## <a name="activate"></a>Aktivovat

Po aktivaci pracovního místa je možné ho zveřejnit a přidat do něho potenciální zákazníky a uchazeče. Možnost přidání potenciálních zákazníků do nabídky volného místa je nastaven v aktivitě Potenciální zákazník v procesu náboru.

> [!NOTE]
> Po aktivaci pracovního místu lze proces náboru aktualizovat.

## <a name="prospects-and-applicants"></a>Potenciální zákazníci a uchazeči

Možnost přidání potenciálních zákazníků do nabídky volného místa je nastavena v [aktivitě Potenciální zákazník](./activities-attract.md#prospect-activity) v procesu náboru. Tato možnost by měla být nastavena před aktivací pracovního místa. Po aktivaci pracovního místa do něho lze přidat potenciální zákazníky a uchazeče.

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

Schválení lze odeslat libovolnému uživateli služby Microsoft Azure Active Directory (Azure AD) ve společnosti. Schválení jsou odeslána současně všem uživatelům, kteří jsou uvedeni jako schvalovatelé. Po schválení pracovního místa je lze aktivovat.

Osoby, které jsou uvedeny jako schvalovatelé, obdrží upozornění v aplikaci Attract s informací, že se mají položku ke schválení. Položka ke schválení se zobrazí také v části **Přiřazené** v řídicím panelu. Jakmile někdo pracovní místo přijme nebo schválí, náborový tým obdrží upozornění. Nakonec obdrží náborový tým upozornění na schválení pracovního místa.

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

    1. Vyberte **+ přidat schvalovatele**a poté zadejte uživatele, který má účet Azure AD. Můžete přidat více schvalujících.
    2. Vyberte **Odeslat schvalovatelům**.

    Pole **Stav práce** v pracovní pozici je nastaveno na **čekající**. Poté, co se hodnota v poli **Stav práce** změní na **Schváleno**, lze pracovní pozici aktivovat.

13. Chcete-li pracovní pozici aktivovat, zaškrtněte políčko **Aktivovat**.
14. Pokud chcete pracovní pozici zveřejnit, přejděte na **Zveřejnit** a vyberte **Zveřejint** na webu Talent Careers nebo LinkedIn.

