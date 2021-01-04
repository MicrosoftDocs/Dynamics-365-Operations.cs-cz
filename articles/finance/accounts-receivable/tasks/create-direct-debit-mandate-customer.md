---
title: Vytvoření zmocnění k přímému debetu pro odběratele
description: Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86d29782f616219b5d84e3567910cb28c60b65ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441050"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Vytvoření zmocnění k přímému debetu pro odběratele

[!include [banner](../../includes/banner.md)]

Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.


## <a name="create-a-bank-account"></a>Vytvoření bankovního účtu
1. V **navigační podokně** přejděte na **Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.
2. V seznamu vyberte záznam. Vyberte například US-001.
3. V podokně akcí klikněte na možnost **Odběratel**.
4. Klikněte na možnost **Bankovní účty**.
5. Klepněte na možnost **Nový**.
6. Zadejte hodnotu do pole **Bankovní účet**.
7. Zadejte hodnotu do pole **Název**.
8. Zadejte hodnotu do pole **IBAN**.
9. Zadejte hodnotu do pole **Měna**.
10. Klikněte na možnost **Uložit**.
11. Zavřete stránku.
12. V **navigačním podokně** přejděte na **Moduly > Správa hotovosti a banky > Bankovní účty > Bankovní účty**.
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. Klikněte na možnost **Upravit**.
16. Rozbalte záložku s náhledem **Další identifikace**.
17. Zadejte hodnotu do pole **ID přímého debetu**.
18. Zadejte hodnotu do pole **IBAN**.
19. Zavřete stránku.
20. Zavřete stránku.

## <a name="define-the-electronic-payment-method"></a>Definování metody elektronické platby
1. V **navigačním podokně** přejděte na **Moduly > Pohledávky > Nastavení plateb > Metody platby**.
2. Klepněte na možnost **Nový**.
3. V poli **Způsob platby** zadejte hodnotu.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Typ platby** zadejte „Elektronická platba“. Typ platby pro metodu platby „zmocnění k přímému debetu“ musí být elektronická platba.
6. Vyberte možnost Ano v poli **Požadovat zmocnění**.
7. Zavřete stránku.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Přidejte zmocnění k přímému debetu zákazníkovi.
1. V **navigační podokně** přejděte na **Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.
2. V seznamu vyberte záznam. Vyberte například US-001.
3. Klikněte na možnost **Upravit**.
4. Rozbalte záložku s náhledem **Výchozí nastavení plateb**.
5. V poli **Metody platby** zadejte nebo vyberte hodnotu.
6. Rozbalte záložku s náhledem **Výchozí nastavení plateb**.
7. Rozbalte záložku s náhledem **Zmocnění k přímému debetu**.
8. Klikněte na tlačítko **Přidat**.
9. V poli **Bankovní účet** zadejte nebo vyberte hodnotu.
10. V poli **Bankovní účet věřitele** zadejte nebo vyberte hodnotu.
11. V poli **Četnost plateb** zadejte počet plateb, u kterých očekáváte, že budou zpracovány pro zmocnění.
12. Klikněte na tlačítko **OK**.
13. Klepněte na položku **Tisk**.
14. Klikněte na **Sestava zmocnění**.
15. Zavřete stránku.
16. Klikněte na možnost **Upravit**.
17. Do pole **Datum podpisu** zadejte datum.
18. Klepněte na tlačítko **Ano**.
19. Zadejte místo podpisu zmocnění.
20. Klikněte na tlačítko **OK**.
21. Zavřete stránku.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vytvoření volné faktury se zmocněním
1. V **podokně navigace** přejděte na **Moduly > Pohledávky > Faktury > Všechny otevřené faktury**.
2. Klepněte na možnost **Nový**.
3. Vyberte odběratele, pro kterého jste vybrali zmocnění.
4. V poli **ID zmocnění k přímému debetu** zadejte nebo vyberte hodnotu.

