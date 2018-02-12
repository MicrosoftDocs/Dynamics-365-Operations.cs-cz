---
title: "Mobilní pracovní prostor správy výdajů"
description: "Toto téma obsahuje informace o mobilním pracovním prostoru Správa výdajů. Tento pracovní prostor umožňuje uživatelům zdokumentovat a odeslat účtenku, aby ji mohli připojit později k sestavě výdajů. Uživatelé mohou také rychle vytvořit řádek výdajů pomocí přiloženého příjmu a vytvořit a spravovat svá vyúčtování výdajů."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: bbbe37330e16a079b817dfe04f4a47f046263e88
ms.contentlocale: cs-cz
ms.lasthandoff: 12/01/2017

---

# <a name="expense-management-mobile-workspace"></a>Pracovnímu prostor správy výdajů

[!include[banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Správa výdajů**. Tento pracovní prostor umožňuje uživatelům zdokumentovat a odeslat účtenku, aby ji mohli připojit později k sestavě výdajů. Uživatelé mohou také rychle vytvořit řádek výdajů pomocí přiloženého příjmu a vytvořit a spravovat svá vyúčtování výdajů. Kromě toho mohou schvalovatelé použít mobilní pracovní prostor **Správa výdajů** k zobrazení vyúčtováí výdajů, která mají přiřazená, a buď schválit nebo zamítnout tato vyúčtování výdajů.


Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Microsoft Dynamics 365 for Unified Operations.


## <a name="overview"></a>Přehled

Mnoho organizací vyžaduje, aby byla připojena k sestavě cestovních nebo obchodních výdajů kopie účtenky, kterou zaměstnanec podává k refundaci. Mobilní pracovní prostor **správy výdajů** umožňuje uživatelům rychlé vytvoření nových řádků výdajů na libovolném mobilním zařízení pomocí připojené fotografie účtenky. Případně mohou uživatelé pořídit fotografii účtenky a připojit ji k sestavě výdajů později. Zaměstnanci také mohou vytvořit a spravovat svá vyúčtování výdajů a pak je posílat ke schválení a úhradě pomocí mobilních zařízení.


Konkrétně mobilní pracovní prostor **Správa výdajů** uživatelům umožňuje provádění těchto úloh:

- Pořízení fotografie účtenky a její nahrání do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Následně můžete připojit uvedenou fotografii k sestavě výdajů později.
- Odešlete soubor jako zdokumentovanou účtenku. Následně můžete připojit uvedený soubor k sestavě výdajů později.
- Vytvořte nový řádek výdajů pomocí připojené účtenky. Později můžete přidat položku řádku k sestavě výdajů a odeslat ke schválení a refundaci.

Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, můžete používat tyto funkce:

- Vytvořte novou sestavu výdajů.
- Transakce kreditních karet a další dříve vytvořené výdaje připojte k vyúčtování výdajů.
- Vytvořte nové výdaje pro vyúčtování výdajů.
- Připojte fotografii účtenky k jakémukoli výdaji ve vyúčtování výdajů, a to buď pořízením její fotografie, nebo nahráním souboru jako záznamu účtenky.
- V závislosti na zásadách výdajů společnosti přidejte seznam hostů do výdaje.
- V závislosti na zásadách výdajů společnosti rozepište výdaje.
- Odešlete vyúčtování výdajů ke schválení a úhradě.
- Schvalte nebo odmítněte vyúčtování výdajů, které jste přiřadili schvalovateli.

## <a name="prerequisites"></a>Požadavky
Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 
Pokud je ve vaší organizaci nasazena aktualizace aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, správce systému musí mobilní pracovní prostor **Správa výdajů** publikovat. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Požadavky, pokud používáte aplikaci Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější
Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací platformy 3 nebo novější, správce systému musí dokončit následující předpoklady. 

<table>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Role</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementujte opravu KB 4019015.</td>
<td>Správce systému</td>
<td>KB 4019015 je X ++ aktualizace nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Správa výdajů</strong>. Pro implementaci KB 4019015 musí správce systému provést tyto kroky:
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stažení opravy hotfix metadat ze služby Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje modely <strong>ApplicationSuite</strong> a <strong>ExpenseMobile</strong> a odešlete ho do služby LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Publikujte <strong>Mobilní pracovní prostor správy výdajů</strong>.</td>
<td>Správce systému</td>
<td>Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Operations
Stáhněte a nainstalujte mobilní aplikaci 365 Dynamics for Unified Operations:

- [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace
1. Spusťte aplikaci na svém mobilním zařízení.
2. Zadejte adresu URL aplikace Dynamics 365.
4. Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
5. Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.


[![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Zdokumentování účtenky pomocí mobilního pracovního prostoru správy výdajů

1. Na svém mobilním zařízení otevřete pracovní prostor **správy výdajů**.
2. Vyberte možnost **Zdokumentovat účtenku**.
3. Vyberte možnost **Pořídit fotografii** nebo **Zvolit obrázek**.
4. Proveďte jeden z následujících kroků:

    - Pokud jste vybrali **Pořídit fotografii**, postupujte následujícím způsobem:

        1. Přejděte k fotoaparátu svého mobilního zařízení, abyste mohli pořídit fotografii účtenku. Poté, co jste pořídili fotografii, klikněte na tlačítko **OK** pro přijetí fotografie.
        2. Volitelné: Zadejte název fotografie a poznámky.

    - Pokud jste vybrali možnost **Zvolit obrázek**, postupujte následujícím způsobem:

        1. V seznamu vyberte obrázek.
        2. Volitelné: Zadejte název obrázku a poznámky.

5. Vyberte **Hotovo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Rychlé zadání výdajů pomocí mobilního pracovního prostoru správy výdajů
1. Na svém mobilním zařízení otevřete pracovní prostor **správy výdajů**.
2. Vyberte **Rychlé zadání výdaje**.
3. Zvolte kategorii pro výdaje. Zobrazí se seznam kategorií výdajů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li vaše kategorie v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte kategorii výdaje nebo přepněte pro hledání podle typu výdaje.
4. Zadejte datum transakce výdaje.
5. Volitelné: Zadejte obchodníka pro výdaje.
6. Zadejte částku výdaje.
7. Vyberte měnu výdaje. Zobrazí se seznam kódů měn, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno až 400 měn, ale vývojář může tento počet změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li vaše měna v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte podle měny nebo přepněte pro hledání podle názvu.
8. Vyberte možnost **Pořídit fotografii** nebo **Zvolit obrázek**.
9. Proveďte jeden z následujících kroků:

    - Pokud zvolíte **Pořídit fotografii**, přejděte k fotoaparátu svého mobilního zařízení, abyste mohli pořídit fotografii účtenku. Poté, co jste pořídili fotografii, klikněte na tlačítko **OK** pro přijetí fotografie.
    - Pokud jste vybrali **Zvolit obrázek**, vyberte obrázek v seznamu.

10. Vyberte **Hotovo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Schvalte sestavu výdajů pomocí mobilního pracovního prostoru Správa výdajů (Pokud používáte aktualizaci z července 2017)
1. Na svém mobilním zařízení otevřete pracovní prostor **správy výdajů**.
2. **Schválení výdajů** zobrazuje počet sestav vyúčtování výdajů, které máte přiřazeny ke schválení. Toto číslo je aktualizována přibližně každých 30minut. Vyberte **Schválení výdajů**.

    Zobrazí se seznam sestav vyúčtování výdajů, které máte přiřazeny ke schválení.
    
3. Vyberte vyúčtování výdajů a zobrazte detaily výdajů.
4. Vyberte vyúčtování výdajů a zobrazte jeho detaily výdajů. Informace, které jsou zobrazeny pro výdaj, obsahují všechny příjemky, hosta a podrobnosti rozpisu.
5. Na stránce **vyúčtování výdajů** vyberte schválení nebo odmítnutí vyúčtování výdajů.
6. Zadejte libovolný komentář pro proces schválení.
7. Vyberte **Hotovo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Vytvořte nové vyúčtování výdajů a odešlete ho ke schválení pomocí mobilního pracovního prostoru Správa výdajů (Pokud používáte aktualizaci z července 2017)
1. Na svém mobilním zařízení otevřete pracovní prostor **správy výdajů**.
2. Vyberte **Zadání výdaje**.
3. Vyberte **Nová sestava** nebo vyberte existující vyúčtování výdajů v seznamu.
4. U nových vyúčtování výdajů zadejte účel a případné doplňkové informace, které jsou k dispozici. Tyto údaje se liší podle toho, jak je vyúčtování výdajů nakonfigurováno pro vaši společnost.
5. Vyberte **Hotovo**.
6. Pokud chcete přidat existující výdaje, jako jsou například transakce platební karty do vyúčtování výdajů, vyberte **Připojit**.
7. Vyberte jeden nebo více výdajů.
8. Vyberte **Hotovo**.
9. Chcete-li do vyúčtování výdajů přidat nový výdaj, vyberte **Nový výdaj**.
10. Zvolte kategorii pro výdaje. Zobrazí se seznam kategorií výdajů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li vaše kategorie v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte kategorii výdaje nebo přepněte pro hledání podle typu výdaje.
11. Volitelné: Zadejte obchodníka pro výdaje.
12. Zadejte datum transakce výdaje.
13. Zadejte částku výdaje.
14. Vyberte měnu výdaje. Zobrazí se seznam kódů měn, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno až 400 měn, ale vývojář může tento počet změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li vaše měna v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte podle měny nebo přepněte pro hledání podle názvu.
15. Vyberte **Hotovo**.
16. Pokud chcete přidat další podrobnosti do výdaje, vyberte **Přidat další podrobnosti**. Pole, která jsou k dispozici, závisí na konfiguraci správy výdajů pro vaši společnost.
17. Pokud zásady společnosti vyžadují příjem pro výdaj, zaškrtněte políčko **Příjmy** a poté proveďte následující kroky:

    1. Vyberte **Zaznamenat příjem** nebo **Připojit účtenku**.
    2. Proveďte jeden z následujících kroků:

        - Pokud jste vybrali možnost **Zaznamenat příjem**, postupujte následujícím způsobem:

            1. Vyberte možnost **Pořídit fotografii** nebo **Zvolit obrázek**.
            2. Proveďte jeden z následujících kroků:

                - Pokud jste vybrali **Pořídit fotografii**, postupujte následujícím způsobem:

                    1. Přejděte k fotoaparátu svého mobilního zařízení, abyste mohli pořídit fotografii účtenku. Poté, co jste pořídili fotografii, klikněte na tlačítko **OK** pro přijetí fotografie.
                    2. Volitelné: Zadejte název fotografie a poznámky.

                - Pokud jste vybrali možnost **Zvolit obrázek**, postupujte následujícím způsobem:

                    1. V seznamu vyberte obrázek.
                    2. Volitelné: Zadejte název obrázku a poznámky.

            3.  Vyberte **Hotovo**.

        - Pokud jste vybrali možnost **připojit příjem**, postupujte následujícím způsobem:

            1.  Vyberte jeden nebo více obrázků v seznamu.
            2.  Vyberte **Hotovo**.

    3. Chcete-li se vrátit k podrobnostem výdaje, klikněte na tlačítko **Zpět**.

18. Pokud zásady společnosti vyžadují hosty pro výdaj, zaškrtněte políčko **Hosté** a poté proveďte následující kroky:

    1. Vyberte **Host**, **Předchozí hosté**, nebo **spolupracovníci**.
    2. Proveďte jeden z následujících kroků:

        - Pokud jste vybrali **Host**, postupujte následujícím způsobem:

            1. Zadejte jméno hosta.
            2. Volitelné: Zadejte organizaci nebo zemi hosta.
            3. Volitelné: Zadejte profesní titul hosta.
            4. Vyberte **Hotovo**.

        - Pokud jste vybrali možnost **Předchozí hosté**, postupujte následujícím způsobem:

            1. Vyberte jednoho nebo více předchozích hostů. Zobrazí se seznam předchozích hostů, které jste přidali do předchozích vyúčtování výdajů, které jsou načteny do aplikací pro použití v offline režimu. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li předchozí host v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte podle jména nebo organizace, země či titulu.
            2. Vyberte **Hotovo**.

        - Pokud jste vybrali **Spolupracovníci**, postupujte následujícím způsobem:

            1. Vyberte jednoho nebo více spolupracovníků. Zobrazí se seznam spolupracovníků, kteří jsou načteni do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li spolupracovník v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte podle jména nebo společnosti či titulu.
            2. Vyberte **Hotovo**.

    3. Chcete-li se vrátit k podrobnostem výdaje, klikněte na tlačítko **Zpět**.

19. Pokud zásady společnosti vyžadují rozepsání výdaje, zaškrtněte políčko **Rozepsat** a poté proveďte následující kroky:

    1. Vyberte první datum k roezpsání.
    2. Vyberte **Přidat rozpis**.
    3. Vyberte podkategorii pro rozepsání výdaje. Zobrazí se seznam podkategorií výdajů, které jsou načteny do vaší aplikace pro použití v režimu offline. Ve výchozím nastavení je načteno 50 položek, ale vývojář může tuto hodnotu změnit. Další informace pro vývojáře najdete v tématu [Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Není-li vaše podkategorie v seznamu, vyberte možnost **Vyhledávat další** k online hledání. Hledejte podle podkategorie výdaje.
    4. Zadejte částku transakce pro rozpis.
    5. Upravte datum transakce, pokud musíte.
    6. Vyberte **Hotovo**.
    7. Opakováním předchozích kroků přidejte všechny rozpisy pro vybrané datum.
    8. Pro další dny můžete vybrat **Kopírovat pro další den** ke zkopírování rozpisu do následujícího dne. Případně můžete vybrat datum k rozepsání a přidat rozepsání stejně jako u počátečního data.
    9. Po dokončení rozepsání výdajů, vyberte tlačítko **Zpět** pro návrat na podrobnosti výdajů.

20. Chcete-li se vrátit k na stránku **Vyúčtování výdajů**, klikněte na tlačítko **Zpět**.
21. Opakováním předchozích kroků dokončete přidání všech výdajů.
22. Vyberte **Odeslat**.
23. Zadejte libovolné komentáře pro schvalujícího.
24. Vyberte **Hotovo**.

