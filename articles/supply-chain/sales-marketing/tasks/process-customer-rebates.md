---
title: Generování a zpracování rabatů odběratelů
description: Tento postup ukazuje zpracování rabatů odběratele z generování nároku až do okamžiku jejich předání do pohledávek jako časově rozlišených položek.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87ddaddb00da50ef9e9e1e7ecf7c3620dabb5a17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209943"
---
# <a name="generate-and-process-customer-rebates"></a>Generování a zpracování rabatů odběratelů

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje zpracování rabatů odběratele z generování nároku až do okamžiku jejich předání do pohledávek jako časově rozlišených položek. Provede vás konkrétním příkladem a vysvětlí vliv různých podmínek na řádcích rabatu na konečné částky, které budou připsány odběrateli. Před spuštěním průvodce je třeba použít ukázková data společnosti USMF a provést následující úkoly: (1) Na stránce Parametry pohledávek rozbalte kartu Ceny a potom kartu Podrobnosti o ceně a zkontrolujte, že je možnost Povolit podrobnosti o ceně nastavena na hodnotu Ano. (2) Na stránce Smlouvy o rabatu vyberte smlouvu o rabatu odběratele: USMF-000001. Pokud pole Stav schválení workflowu není nastaveno na Schváleno, proveďte schválení kliknutím na Ověření v podokně akcí.


## <a name="review-a-customer-rebate-agreement"></a>Kontrola smlouvy o rabatu odběratele
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Rabaty odběratele > Smlouvy o rabatu**.
    - Příštích několik kroků je zaměřeno na podmínky smlouvy USMF-000001. Snadněji tak porozumíte způsobu výpočtu hodnoty úvěru odběratele později v rámci postupu.  
    - Smlouva je pro jednoho odběratele, v tomto příkladu pro odběratele US-009.  
    - Rabaty jsou odběrateli poskytnuty v případě nákupu určitého produktu. V tomto případě to je produkt s číslem položky T0020.   
    - Prodejní výsledky odběratele, podle kterých se vytváří odhad částky rabatu, je nutné kumulovat jednou týdně.  
    - Nastavení „Cena převzata z“ je Brutto, což znamená, že částka prodeje tohoto řádku, na základě které je odhadován nárok, není snížena řádkovou slevou.  
    - V poli Typ zalomení řádku rabatu se zobrazuje metoda pro výpočet rabatů. V tomto případě je prodejní cíl, podle kterého se mají rabaty odhadovat, nastaven na Množství.   
    - Řádky smlouvy specifikují typ částky rabatu, skutečnou hodnotu rabatu a prahové hodnoty. V tomto příkladu bude mít odběratel nárok na rabat ve výši 20 USD za prodanou jednotku, pokud jeho týdenní nákup produktu bude spadat do rozmezí 1 až 50 jednotek, a rabat ve výši 40 USD, pokud zakoupí více než 50 jednotek.  
2. Zavřete stránku.

## <a name="generate-rebate-claims"></a>Generování nároků na rabat
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. Klepněte na možnost **Nový**. K napodobení způsobu generování nároků na rabat je třeba vytvořit prodejní objednávku, kde produkt a množství zajistí danému odběrateli nárok na rabat.    
3. V poli **Účet odběratele** zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko **OK**.
5. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
6. Nastavte **Množství** na hodnotu 40.
7. V části **řádky prodejní objednávky** vyberte **řádek prodejní objednávky**.
8. Klikněte na možnost **Podrobnosti o ceně**. Není-li tato možnost zobrazena, je to tím, že před spuštěním průvodce nebyla nastavena možnost **Povolit podrobnosti o ceně** na hodnotu Ano.     
9. Rozbalte oddíl **Rabaty**. Na kartě **Rabaty** jsou uvedeny všechny smlouvy o rabatu, které lze použít pro aktuální řádek objednávky, a také zde je odhad částky rabatu. Zobrazené částky jsou pouze indikace možných budoucích nároků na rabat. Částky skutečných rabatů se mohou lišit v závislosti na celkovém objemu prodeje dosaženému odběratelem v rámci periodické smlouvy o rabatu, na tom, zda odběratel vrátil veškeré nebo částečné množství a zda byla fakturována platná prodejní objednávka.
10. Zavřete stránku.
11. Klikněte na **Přidat řádek**.
12. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
13. Nastavte **Množství** na hodnotu 60.
14. Klikněte na možnost **Uložit**.
15. V **podokně akcí** klikněte na **Faktura**.
16. Klikněte na **Faktura**.
17. Rozbalte sekci **Parametry**.
18. V poli **Množství** vyberte možnost „Vše“.
19. Klikněte na tlačítko **OK**.
20. Klikněte na tlačítko **OK**.

## <a name="process-rebate-claims"></a>Nároky na rabat procesu
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Rabaty odběratele > Rabaty**.
    - Stránka Rabaty funguje jako pracovní plocha, kde můžete kontrolovat, schvalovat a zpracovat nároky na rabat. Nyní budete zpracovávat nároky, které byly vytvořeny v důsledku fakturace prodejní objednávky pro odběratele US-009, na kterého platí smlouva o rabatu USMF-000001.   
    - První řádek představuje nároku na rabat 800 USD, který je založen na prodeji 40 jednotek produktu T0020 (vypočteno 20 USD za jednotku). To odpovídá podmínkám první množstevní kategorie ve smlouvě o rabatu.  
    - Druhý nárok je 2 400 USD založený na prodeji 60 jednotek produktu T0020 (vypočítáno 40 USD za jednotku) podle druhé množstevní kategorie ve smlouvě.  
    - Oba nároky jsou ve stavu „K výpočtu“. To znamená, že jsou přidruženy ke smlouvě, která slouží ke sledování prodejních výsledků zákazníka v pravidelných intervalech, a že musí být přepočítávány kvůli zohlednění celkového objem prodeje za příslušné období.   
2. Klikněte na možnost **Kumulovat**.
3. V poli **Odběratel** zadejte nebo vyberte hodnotu.
4. V poli **Počáteční datum** vyberte aktuální datum.
5. Klikněte na tlačítko **OK**. Po spuštění funkce **Kumulovat** se provede úprava odhadu částky nároku zohledňující skutečnost, že je celkový objem prodeje odběratele za příslušné období vyšší než při prvním generování rabatu. Vzhledem k tomu, že celkové nakoupené množství dosáhlo počtu 100 jednotek, odběratel nyní má nárok na 40 USD za jednotku (podle druhé množstevní kategorie smlouvy) nebo 400 USD celkového rabatu. Rozdíl je zaznamenán jako nová "úprava" nároku pro dalších 800 USD. Stav nároků na rabat, které byly zahrnuty v kumulované aktualizaci, je nyní nastaven na hodnotu Vypočteno. 
6. V seznamu označte všechny řádky.
7. Klikněte na **Schválit**.
8. Klikněte na možnost **Zpracovat**.
9. V poli **Odběratel** zadejte nebo vyberte hodnotu.
10. Klikněte na tlačítko **OK**. Zpráva ukazující, že byl rabat úspěšně zpracován a že se stav nároku změnil na hodnotu Označit. To znamená, že v důsledku zaúčtování deníku časového rozlišení rabatu:
    - Nároky byly nyní převedeny do dočasného zůstatku odběratele jako odpočty.
    - Na účet časového rozlišení rabatu bylo provedeno připsání představující budoucí odpovědnost směrem k odběrateli.
    - Z výdajového účtu rabatu byl proveden odpis v rámci uznání vzniklých nákladů v souvislosti s prodejem.   

