---
title: "Import souborů ISO20022"
description: "Toto téma popisuje, jak importovat soubory plateb formátů ISO 20022 camt.054 a pain.002 do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>Import souborů ISO20022

## <a name="overview"></a>Přehled
Můžete importovat soubory plateb, které mají následující formáty:

 - **Avízo o kreditní transakci ISO20022 camt.054** – Importuje příchozí platby do deníku plateb odběratele ze souboru v tomto formátu.
 - **Vrácení stavu ISO20022 pain.002** a **Avízo o debetní transakci ISO20022 camt.054** – Importuje soubory vrácení v těchto formátech do deníku plateb závazků převodu.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Předpoklady pro import souboru platebního avíza camt.054
Import zpráv s bankovními oznámeními ve formátu camt.054.001.002 do deníku plateb odběratele vyžaduje splnění následujících předpokladů.

1. Importujte konfiguraci **ISO20022 camt.054** Electronické výkaznictví (ER) z aplikace Microsoft Dynamics Lifecycle Services (LCS). Potom na stránce **Způsob platby odběratele** v poli **Importovat konfigurace formátu** vyberte konfiguraci. Další informace naleznete v tématu [Formáty souboru pro způsoby platby](emea-select-file-formats-for-the-method-of-payments.md).
2. Na stránce **Všichni zákazníci** zadejte název a číslo organizace pro každého zákazníka.
3. Na stránce **Bankovní účet odběratele** nastavte bankovní účet záznamu odběratele zadáním následujících informací: IBAN nebo číslo bankovního účtu a kód SWIFT nebo směrové číslo.
4. Na stránce **Bankovní účty** nastavte bankovní účty právnické osoby zadáním následujících informací: IBAN nebo číslo bankovního účtu, kód SWIFT nebo směrové číslo, měna a adresa.

    > [!NOTE]
    > Pokud budete používat rozšířené bankovní odsouhlasení, na pevné záložce **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení bankovního výpisu** na **Ano**. Pokud chcete odsouhlasit nezaúčtované importované platby, nastavte možnost **Použít bankovní výpisy jako potvrzení elektronické platby** na **Ano**.

5. Volitelné: Na kartě **Mapování kódu transakce** nastavte mapování mezi kódy bankovních transakcív souboru a typy bankovních transakcí.
6. Pokud soubor obsahuje poplatky za transakce, které chcete zaúčtovat spolu s příchozí platbou, vytvořte pro platební poplatek na stránce **Platební poplatky odběratele**. Poté na stránce **Způsoby platby** přidružte platební poplatek k bankovnímu účtu v nastavení platebního poplatku.
7. Pokud budou importovány platby ESR a budou obsahovat odkazy ISR (k dispozici pro právnické osoby ve Švýcarsku), proveďte následující nastavení:

    - V poli **Platby odběratele, délky účtu** zadejte délku kódu odběratele, který se používá v referencích ISR nebo pro automatickou identifikaci odběratele.
    - Ujistěte se, že číslo odběratele a čísla faktury (číselné řady) obsahují pouze číslice. Nesmí obsahovat žádné jiné znaky. Číslo faktury nesmí obsahovat počáteční nuly.
    - Zadejte ESR, BESR a směrové číslo pro bankovní účet pro právní subjekt. Další informace naleznete v tématu [starší funkce ESR](emea-che-esr-customer-payments-import.md), protože jsou požadována podobná nastavení.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Import souboru kreditního avíza camt.054 do deníku plateb odběratele
1. Na stránce **Řádky deníku plateb odběratele** klikněte na **Funkce** > **Import plateb**.
2. Vyberte metodu platby, která má požadované nastavení pro formát camt.054 ISO20022.
3. Zadejte požadované parametry a cestu k souboru a klepněte na tlačítko **OK**.

Soubor je importován.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Předpoklady pro import souborů se stavem pain.002 a Avízo o debetní transakci camt.054 do deníku plateb závazků převodu
Import bankovních zpráv v následujících formátech ISO20022 na stránku **Převod platby dodavatele** vyžaduje splnění následujících předpokladů: zprávy o stavu vrácení pain.002.001.003 a debetní avízo camt.054.001.002.

1. Importujte konfiguraci **ISO20022 camt.054** a **ISO20022 pain.002** ER z LCS.
2. Na stránce **Způsob platby dodavatele** v polích **Konfigurace formátu vrácení** a **Sekundární konfigurace formátu vrácení** vyberte importované konfigurace ER. Je třeba aktivovat obecný elektronický formát vrácení pro vybranou metodu platby.
3. Na stránce **Mapování stavu formátu vrácení** nastavte mapování kódů stavu mezi stavy pain.002 a stavy deníku plateb dodavatele.

    Následuje příklad nastavení stavu.

    Stav vrácení | Stav platby
    --------------|---------------
    RJCT          | Odmítnuto
    ACCP          | Akceptováno
    ACSP          | Přijato

4. Na stránce **Kódy chyb formátu pro výpis** nastavte kódy chyb a popisy pain.002 v souladu s externími stavovými kódy důvodu ISO20022.

    Následuje příklad součásti nastavení kódu chyby.

    Kód | Jméno
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Pokud soubor camt.054 obsahuje poplatky za transakce, které chcete zaúčtovat spolu s příchozí platbou, vytvořte pro platební poplatek na stránce **Platební poplatky dodavatele**. Poté na stránce **Způsoby platby** přidružte platební poplatek k bankovnímu účtu v nastavení platebního poplatku.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Importujte soubor vrácení stavu pain.002 nebo debetního avíza camt.054 do deníku plateb dodavatele
1. Otevřete stránku **Platební převody** v nabídce Závazky.
2. Na stránce **Převody plateb** klikněte na **Soubor vrácení – dodavatel**.
3. Vyberte metodu platby, která má požadované nastavení pro soubory ISO20022, a klikněte na tlačítko **OK**.
4. Vyberte formát souboru, který chcete importovat, a klikněte na tlačítko **OK**.
5. Zadejte požadované parametry a cestu k souboru a klepněte na tlačítko **OK**.

Při importu souboru pain.002 se aktualizuje stav řádků platby dodavatele na základě informací v importovaném souboru.

Při importu souboru camt.054 byste měli zadat následující další parametry:

- **ID poplatku** – zadejte ID poplatku, které bude definovat nové řádky poplatků plateb, které budou vytvořeny na řádku deníku plateb dodavatele, pokud je k dispozici v souboru camt.054.
- **Název nového deníku** a **Popis nového deníku** – zadejte název a popis deníku, do kterého budou převedeny zpracované transakce. Po převodu je nutné přiřadit v novém deníku nová čísla dokladů.
- **Import transakcí přímého debetu** – Nastavte tuto možnost na **Ano**, pokud odchozí přímé debety musí být importovány do deníku plateb dodavatele.
- **Název deníku** – Definujte nový název deníku pro importované transakce přímého debetu.
- **Vyrovnat transakce** – nastavte tuto možnost na **Ano**, pokud musí být importované platby dodavatele vyrovnány s fakturami, které jsou nalezeny v systému.

Můžete zobrazit importované informace na stránce **Platební převody**. 

