---
title: Vytvoření odpisového deníku pro odběratele
description: Tento průvodce úkolem znázorňuje, jak nastavit parametry pro odpisy a potom odepsat transakce ze stránky Kolekce, stránky Otevřené faktury odběratele a stránky Odběratel.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6526e57cf2ed84161eb7a92c031127bb6c6536a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003293"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Vytvoření odpisového deníku pro odběratele

[!include [banner](../../includes/banner.md)]

Tento průvodce úkolem znázorňuje, jak nastavit parametry pro odpisy a potom odepsat transakce ze stránky Kolekce, stránky Otevřené faktury odběratele a stránky Odběratel. Tento úkol využívá ukázkovou společnost USMF.


## <a name="set-up-the-write-off-parameters"></a>Nastavení parametrů odpisu
1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Parametry pohledávek**.
2. Klikněte na kartu **Inkasa**.
3. Rozbalte nebo sbalte oddíl **Odpis**.
    - **Odpisový deník** je deník hlavní knihy, který bude obsahovat transakce odpisů, které jste vytvořili.  
    - Pro každý odpis lze přiřadit kód důvodu. Toto výchozí nastavení můžete v době odpisu kdykoli přepsat.  
    - Nastavením hodnoty **Samostatná DPH** na Ano umožníte oddělení DPH z původní transakce v odpisu.  
4. Zavřete stránku.
5. Přejděte na **Kredit a inkasa > Nastavení > Účetní profily odběratele**. Účet odpisu bude použit jako účet nákladů nebo úpravy rezerv v deníku hlavní knihy.
6. Zavřete stránku.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Odpis zůstatku zákazníka ze stránky Splatné zůstatky
1. Přejděte do nabídky **Kredit a inkasa > Inkasa > Splatné zůstatky**.
2. Označte řádek pro odběratele, který chcete odepsat. Označte například řádek obsahující společnost Birch Company.
3. V **podokně akcí** klikněte na **Shromáždit**.
4. Klikněte na **Odepsat**.
5. Klikněte na tlačítko **OK**.
6. Zavřete stránku.
7. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Položky deníku > Hlavní deníky**.
8. Vyberte číslo dávky deníku pro deník, který obsahuje váš odpis. Je vytvořen jeden řádek pro storno zůstatku odběratele. Jeden nebo více řádků jsou vytvořeny pro zaúčtování odpisů na účet odpisu.  
9. Zavřete stránku.
10. Zavřete stránku.

## <a name="write-off-transactions-from-the-collections-form"></a>Odpisové transakce z inkasního formuláře.
1. Přejděte do nabídky **Kredit a inkasa > Inkasa > Splatné zůstatky**.
2. Vyberte jméno odběratele, který obsahuje transakce, které chcete odepsat. Vyberte například Cave Wholesales (US-004).
3. Označte řádek pro první transakci.
4. Označte řádek pro druhou transakci.
5. Klikněte na **Odepsat**.
6. Zadejte údaj Pochybné pohledávky do pole **Komentář k důvodu**.
7. Klikněte na tlačítko **OK**.
8. Zavřete stránku.
9. Zavřete stránku.
10. Přejděte do nabídky **Hlavní kniha > Položky deníku > Hlavní deníky**.
11. Vyberte číslo dávky deníku pro deník, který obsahuje váš odpis. Je vytvořen jeden řádek pro storno zůstatku odběratele. Jeden nebo více řádků jsou vytvořeny pro zaúčtování odpisů na účet odpisu.  
12. Zavřete stránku.
13. Zavřete stránku.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Odepsání faktury ze stránky Otevřené faktury odběratelů
1. Přejděte na **Navigační podokno > Moduly > Pohledávky > Faktury > Otevřené faktury odběratele**.
2. Označte řádek pro fakturu. Například označte řádek pro CIV-000667.
3. V **podokně akcí** klikněte na **Faktura**.
4. Klikněte na **Odepsat**.
5. Klikněte na tlačítko **OK**.
6. Zavřete stránku.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Odpis zůstatku odběratele ze strany zákazníka
1. Přejděte na **Pohledávky > Odběratelé > Všichni odběratelé**.
2. Výběr účtu zákazníka. Vyberte například USA-001 (Maloobchod Contoso pro San Diego).
3. V **podokně akcí** klikněte na **Shromáždit**.
4. Klikněte na **Odepsat**.
5. Klikněte na tlačítko **OK**.
6. Zavřete stránku.

