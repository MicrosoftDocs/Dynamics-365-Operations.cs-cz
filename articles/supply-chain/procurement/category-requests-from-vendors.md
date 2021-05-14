---
title: Požadavky kategorií od dodavatelů
description: Toto téma popisuje, jak mohou prodejci pro svůj účet požadovat kategorie nákupu. Popisuje také proces schvalování, který provádějí agenti nákupu.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fb3555e6d923fe37479c3204f0b78f7cdf510118
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938431"
---
# <a name="category-requests-from-vendors"></a>Požadavky kategorií od dodavatelů

[!include [banner](../includes/banner.md)]

Proces žádosti o kategorii umožňuje, aby prodejci požadovali přidružení nových kategorií zakázek k jejich účtu. Tyto kategorie zadávání zakázek pak mohou být použity souvisejícími procesy zadávání zakázek a získávání zdrojů. (Další informace viz [Přehled katalogů zakázek](procurement-catalogs.md).)

Žádosti o kategorii iniciují prodejci v pracovním prostoru **Informace o prodejci**. Poté jsou odeslány vaší agentuře ke kontrole a schválení. Schválené kategorie se přidají do seznamu kategorií zásobování pro účet dodavatele.

## <a name="turn-on-the-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Pokud váš systém ještě neobsahuje funkci popsanou v tomto tématu, přejděte na [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Umožnit dodavatelům žádat o kategorie zásobování prostřednictvím spolupráce s dodavateli*.

Po zapnutí této funkce můžete do účtů dodavatelů stále ručně přidávat kategorie zásobování. Pro informace viz [Schválení dodavatelů pro konkrétní kategorie zásobování](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Požadavky na schválení dodavatele

Než může prodejce komunikovat s požadavky na kategorii, musí být nastaven pro spolupráci s dodavatelem.

Dodavatel musí mít alespoň jednoho uživatele spolupráce dodavatele. Pouze uživatelé dodavatelů, kteří mají jednu nebo obě z následujících rolí zabezpečení, mohou vytvářet a odesílat požadavky na kategorie:

- Kontakt dodavatele (externí)
- Správce dodavatele (externí)

Další informace o naleznete v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Nastavení workflow žádosti o kategorii dodavatele

Workfloe *Žádost o kategorii dodavatele* musí být nastavena ve workflow zásobování a získávání zdrojů. Prodejci odešlou nové žádosti o kategorie, které můžete zkontrolovat a schválit. Po schválení požadavku na kategorii se do účtu dodavatele přidají požadované kategorie zásobování.

Následující příklad ukazuje, jak nastavit jednoduchý workflow *Žádost o kategorii dodavatele*, který má jediného schvalovatele. Musíte zkontrolovat své interní procesy a určit vhodné nastavení workflow pro vaši agenturu.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Workflow modulu Zásobování a zdroje**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně vyberte **Workflow požadavku na kategorii dodavatele** a otevřete editor workflow.
1. Přihlaste se do editoru workflow.
1. V podokně akcí zvolte **Vlastnosti**.
1. Na stránce **Vlastnosti** pro workflow v poli **Pokyny k odeslání** zadejte text pokynu. Pokyny budou viditelné pro dodavatele, když podají žádost o kategorii.
1. Zavřete stránku **Vlastnosti**.
1. Přetáhněte prvek worklflowu **Schválit nový požadavek na kategorii** na plátno.
1. Přetáhněte odkaz z prvku worklflowu **Start** do prvku workflowu **Schválit nový požadavek na kategorii**.
1. Přetáhněte odkaz z prvku workflowu **Schválit nový požadavek na kategorii** do prvku workflowu **Konec**.
1. Poklepejte (nebo dvakrát klikněte) na prvek workflowu **Schválit nový požadavek na kategorii**.
1. Vyberte a podržte (nebo na něj klikněte pravým tlačítkem) prvek workflowu **Krok 1** a poté vyberte **Vlastnosti**.
1. Na stránce **Vlastnosti** pro prvek workflowu v poli **Předmět pracovní položky** zadejte text předmětu. Tento text se zobrazí jako hodnota pole **Předmět** na stránce **Pracovní položky, které mi byly přiděleny**.
1. Do pole **Pokyny pracovní položky** zadejte text pokynů. Pokyny budou viditelné pro schvalovatele, jakmile vybere **Workflow** v podokně Alce žádosti o kategorii.
1. V levém podokně vyberte **Přiřazení**.
1. Na kartě **Typ přiřazení** nastavte **Přiřadit uživatele do tohoto prvku workflowu** na *Uživatel*.
1. Na kartě **Uživatel** v seznamu **Dostupní uživatelé** vyberte schvalovatele. Vyberte například uživatele v oddělení zásobování.
1. Vyberte tlačítko pravé šipky (**\>**) a přesuňte schvalovatele do seznamu **Vybraní uživatelé**.
1. Zavřete stránku **Vlastnosti**.
1. Zvolte **Uložit a zavřít**.
1. Do pole **Poznámky k verzi** zadejte poznámky o workflowu.
1. Zvolte **OK** pro uložení workflowu.
1. Pokud jste připraveni zahájit testování workflowu, vyberte **Aktivovat novou verzi**. Jinak vyberte **Neaktivovat novou verzi**.
1. Nastavení workflowu dokončíte tlačítkem **OK**.

> [!TIP]
> Pokud vaše agentura nevyžaduje schválení žádostí o kategorii, měli byste nakonfigurovat workflow pro automatické schválení.

Další informace o nastavování workflowů naleznete v tématu [Přehled systému workflow](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Vytvoření a odeslání požadavku na kategorii

Tato část popisuje, jak mohou prodejci používat pracovní prostor **Informace o prodejci** pro vytváření, úpravy, zobrazení a odesílání požadavků na kategorie.

### <a name="start-a-new-request"></a>Zahájení nového požadavku

Chcete-li zahájit nový požadavek na kategorii, postupujte takto.

1. V pracovním prostoru **Informace o prodejci** vyberte dlaždici **Žádosti o kategorii**.
1. Na stránce **Žádosti o kategorii** v podokně Akce vyberte **Nová žádost o kategorii**.
1. V dialogovém okně **Nová žádost o kategorii** vyhledejte kategorii, o kterou chcete žádat, procházením stromu nebo použitím filtru v horní části seznamu. Zaškrtněte políčko u každé příslušné kategorie.

    Mějte na paměti následující body:

    - Kategorie, které jsou aktuálně aktivní na vašem účtu dodavatele, jsou zobrazeny jako vybrané a nelze je odebrat.
    - V jedné žádosti o kategorii můžete požádat o více kategorií zásobování.

1. Výběrem **OK** vytvoříte novou žádost konceptu.

    Nový koncept požadavku se nyní objeví na stránce **Žádosti o kategorii**.

1. Otevřete novou žádost o koncept, zkontrolujte ji a podle potřeby upravte.

    - Chcete-li zobrazit seznam kategorií, které jsou aktuálně zahrnuty v požadavku, vyberte rychlou kartu **Požadované kategorie**.
    - Chcete-li zobrazit aktivní kategorie, otevřete okno s fakty **Aktivní kategorie** na pravé straně stránky.
    - Chcete-li do požadavku přidat kategorii, vyberte **Přidat** na panelu nástrojů na rychlé kartě **Požadované kategorie**.
    - Chcete-li z požadavku odebrat kategorii, vyberte kategorii na rychlé kartě **Požadované kategorie** a poté vyberte **Odstranit** na panelu nástrojů.
    - Chcete-li k žádosti připojit dokument, vyberte **Přílohy** v podokně Akce. Přiložené dokumenty budou k dispozici schvalovatelům při kontrole žádosti o kategorii.
    - Chcete-li od žádosti odebrat připojený dokument, vyberte **Přílohy** v podokně Akce. Vyberte dokument, který chcete odebrat, a poté vyberte **Odstranit** v podokně Akce.

1. Pokud jste připraveni odeslat požadavek, vyberte **Odeslat** v podokně akcí. V opačném případě jednoduše zavřete stránku a přeskočte zbývající kroky tohoto postupu. Poté se můžete k žádosti vrátit později.
1. Přečtěte si všechny zobrazené pokyny k odeslání a poté vyberte **Odeslat**.
1. Do pole **Komentář** zadejte jakékoli další požadované informace. Poté zvolením možnosti **Odeslat** požadavek dokončete.

### <a name="edit-a-draft-or-recalled-request"></a>Úprava konceptu nebo staženého požadavku

Chcete-li upravit koncept nebo požadavek na kategorii, postupujte takto.

1. V pracovním prostoru **Informace o prodejci** vyberte dlaždici **Žádosti o kategorii**.
1. Vyberte koncept nebo stažený požadavek a otevřete ho.
1. Podle potřeby upravte požadavek a poté ho buď zavřete, nebo odešlete, jak je popsáno v předchozím postupu.

### <a name="submit-a-draft-or-recalled-request"></a>Odeslání konceptu nebo staženého požadavku

Chcete-li odeslat koncept nebo požadavek na kategorii, postupujte takto.

1. V pracovním prostoru **Informace o prodejci** vyberte dlaždici **Žádosti o kategorii**.
1. Vyberte koncept nebo odvolaný požadavek, který chcete odeslat.
1. V podokně Akce klikněte na možnost **Odeslat**.
1. Přečtěte si všechny zobrazené pokyny k odeslání a poté vyberte **Odeslat**.
1. Do pole **Komentář** zadejte jakékoli další požadované informace. Poté zvolením možnosti **Odeslat** požadavek dokončete.

    Stav požadavku na kategorii se změní na jednu z následujících hodnot:

    - _Čekající na kontrolu_ – požadavek je ve workflowu.
    - _Čeká na schválení_ – Je vyžadováno schválení.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Odvolání odeslané žádosti, která dosud nebyla schválena

Chcete-li odvolat požadavek na kategorii, který byl odeslán, ale ještě nebyl schválen, postupujte takto.

1. V pracovním prostoru **Informace o prodejci** vyberte dlaždici **Žádosti o kategorii**.
1. Vyberte nevyřízenou žádost, kterou chcete odvolat.
1. V podokně akcí zvolte **Odvolat**.
1. Do pole **Zadat komentář** zadejte jakékoli další požadované informace. Poté zvolením možnosti **Odeslat** požadavek dokončete.

    Stav požadavku na kategorii na se změní na _Zrušeno_. Žádost zůstane v tomto stavu, dokud ji nesmažete nebo znovu neodešlete.

### <a name="delete-a-draft-or-recalled-request"></a>Odstranění konceptu nebo staženého požadavku

Chcete-li odstranit koncept nebo požadavek na kategorii, postupujte takto.

1. V pracovním prostoru **Informace o prodejci** vyberte dlaždici **Žádosti o kategorii**.
1. Vyberte koncept nebo odvolaný požadavek, který chcete odstranit.
1. V podokně Akce zvolte **Odstranit**.
1. Vyberte **Ano** pro potvrzení odstranění.

### <a name="view-completed-requests"></a>Zobrazení dokončených žádostí

Chcete-li zobrazit dokončené žádosti, otevřete pracovní prostor **Informace o prodejci** a vyberte dlaždici **Žádosti o kategorii**. Dokončené žádosti o kategorii budou mít jeden z následujících stavů:

- _Schváleno_ – Žádost byla schválena. Chcete-li zobrazit nově přidané kategorie, přejděte zpět na pracovní prostor **Informace o prodejci**, otevřete rozevírací seznam **Více informací** rozevírací v levém podokně a poté vyberte **Kategorie**.
- _Odmítnuto_ – Žádost byla zamítnuta. Podle potřeby můžete vytvořit nový požadavek na kategorii.

## <a name="review-category-requests"></a>Kontrola žádostí o kategorii

Tato část vysvětluje, jak schvalovat, odmítat a delegovat žádosti o kategorie, které dodavatelé odeslali, a jak zobrazit dokončené žádosti. Tyto akce workflowu jsou pro celou žádost o kategorii.

### <a name="view-category-requests"></a>Zobrazení žádostí o kategorii

Chcete-li zobrazit žádosti o kategorii, postupujte takto.

1. Přejděte do nabídky **Zásobování a získávání zdrojů \> Dodavatelé \> Žádosti o spolupráci s dodavateli \> Žádosti o kategorii**.

    Zobrazí se stránka **Žádosti o kategorii**. Výchozí zobrazení stránky zobrazuje požadavky na kategorie, které mají stav *Čekající akce*.

1. Chcete-li zobrazit všechny požadavky, vyberte *Vše* v poli **Zobrazit žádosti**.
1. Otevřete žádost, zkontrolujte ji a podle potřeby upravte.

    - Chcete-li zobrazit seznam kategorií, které jsou aktuálně zahrnuty v požadavku, vyberte rychlou kartu **Požadované kategorie**.
    - Chcete-li zobrazit aktivní kategorie, otevřete okno s fakty **Aktivní kategorie** na pravé straně stránky.
    - Pokud byly odeslány dokumenty, tlačítko **Přílohy** (kancelářská sponka) v podokně Akce zobrazuje počet přiložených dokumentů. Chcete-li zobrazit připojené dokumenty, vyberte tlačítko **Přílohy**. Poté vyberte dokument, který chcete zobrazit, a zobrazte ho výběrem možnosti **Otevřít**.
    - Chcete-li k žádosti připojit dokument, vyberte **Přílohy** v podokně Akce. Přiložené dokumenty budou k dispozici schvalovatelům při kontrole žádosti o kategorii.
    - Chcete-li od žádosti odebrat připojený dokument, vyberte **Přílohy** v podokně Akce. Vyberte dokument, který chcete odebrat, a poté vyberte **Odstranit** v podokně Akce.
    - Chcete-li vybrat historii workflowu, vyberte **Workflow** v podokně Akce. V možnostech workflowu vyberte **Více** a pak **Historie workflowu**. Zobrazí se stránka **Historie workflowu**.

### <a name="approve-a-pending-category-request"></a>Schválení nevyřízeného požadavku na kategorii

Chcete-li schválit nevyřízenou žádost o kategorii, postupujte takto.

1. Přejděte do nabídky **Zásobování a získávání zdrojů \> Dodavatelé \> Žádosti o spolupráci s dodavateli \> Žádosti o kategorii**.
1. Vyberte nevyřízenou žádost ke schválení.
1. Zkontrolujte žádost o kategorii.
1. Volitelné: Na rychlé kartě **Všeobecné** v poli **Kód důvodu** vyberte kód důvodu. Poté v poli **Komentář důvodu** zadejte komentář o kódu důvodu.
1. V podokně akcí zvolte **Workflow**.
1. V možnostech workflowu vyberte **Schválit**.
1. Do pole **Komentář** zadejte jakékoli další požadované informace. Poté zvolením možnosti **Schválit** požadavek dokončete.

    Stav požadavku na kategorii se změní na _Schválený_ a na účet dodavatele se přidají kategorie zásobování.

### <a name="reject-a-pending-category-request"></a>Zamítnutí nevyřízeného požadavku na kategorii

Chcete-li zamítnout nevyřízenou žádost o kategorii, postupujte takto.

1. Přejděte do nabídky **Zásobování a získávání zdrojů \> Dodavatelé \> Žádosti o spolupráci s dodavateli \> Žádosti o kategorii**.
1. Vyberte nevyřízenou žádost k zamítnutí.
1. Zkontrolujte žádost o kategorii.
1. V podokně akcí vyberte **Upravit**.
1. Na rychlé kartě **Všeobecné** v poli **Kód důvodu** vyberte kód důvodu. Poté v poli **Komentář důvodu** zadejte komentář o kódu důvodu.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí zvolte **Workflow**.
1. V možnostech workflowu vyberte **Více** a pak **Zamítnout**.
1. Do pole **Komentář** zadejte jakékoli další požadované informace. Poté zvolením možnosti **Zamítnout** požadavek dokončete.

    Stav požadavku na kategorii na se změní na _Zamítnuto_. V tomto okamžiku může prodejce podle potřeby vytvořit nový požadavek na kategorii.

### <a name="delegate-a-pending-category-request"></a>Delegování nevyřízeného požadavku na kategorii

Chcete-li delegovat nevyřízenou žádost o kategorii na jiného uživatele, postupujte takto.

1. Přejděte do nabídky **Zásobování a získávání zdrojů \> Dodavatelé \> Žádosti o spolupráci s dodavateli \> Žádosti o kategorii**.
1. Vyberte nevyřízenou žádost, kterou chcete schválit.
1. V podokně akcí zvolte **Workflow**.
1. V možnostech workflowu vyberte **Více** a pak **Delegovat**.
1. V poli **Uživatel** vyberte uživatele, kterému chcete přiřadit požadavek na kategorii ke kontrole.
1. Do pole **Komentář** zadejte jakékoli další požadované informace.
1. Delegaci dokončíte tlačítkem **Delegovat**. Vybraný uživatel nyní může zkontrolovat požadavek na kategorii.

### <a name="view-procurement-categories-for-a-vendor"></a>Zobrazení kategorií zásobování pro dodavatele

Chcete-li po schválení požadavku na kategorii zobrazit kategorie zásobování pro dodavatele, postupujte následovně.

1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.
1. Na stránce **Všichni dodavatelé** vyberte dodavatele, pro kterého chcete zobrazit kategorie zásobování.
1. V podokně akcí otevřete kartu **Obecné** a ve skupině **Nastavení** vyberte **Kategorie**.

    Zobrazí se stránka **Kategorie**. Na rychlé kartě **Zásobování** jsou kategorie nákupu, které byly přidány prostřednictvím požadavku na kategorii.

1. Na rychlé kartě **Zásobování** můžete v případě potřeby provést změny. Můžete například nastavit pole **Stav kategorie dodavatele** na _Upřednostňováno_.
