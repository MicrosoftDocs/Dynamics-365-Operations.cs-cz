---
title: "Přehled objednávek odběratele"
description: "Toto téma obsahuje informace o objednávkách odběratele v Retail Modern POS (MPOS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f68f9dce544256a2b1a9927f019a676a6845f46d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="customer-orders-overview"></a>Přehled objednávek odběratele

[!include[banner](includes/banner.md)]


Toto téma obsahuje informace o objednávkách odběratele v Retail Modern POS (MPOS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích.

Ve světě omni-channel maloobchodu celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele neboli speciálních objednávek, aby splnili různé požadavky týkající se produktu a plnění. Zde jsou některé typické scénáře:

-   Zákazník chce, aby produkty byly doručeny k určitému datu na konkrétní adresu.
-   Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil.
-   Zákazník chce, aby zakoupené produkty vyzvedl někdo jiný.

Maloobchodní prodejci také používají objednávky odběratele pro minimalizaci ztrát prodeje, které by jinak výpadky zásob mohly způsobit, protože zboží lze doručit nebo vyzvednout v jiném čase nebo na jiném místě.

## <a name="set-up-customer-orders"></a>Nastavení objednávek odběratele
Zde jsou některé parametry, které lze nastavit na stránce **Parametry maloobchodu** za účelem definování způsobu plnění objednávek odběratele:

-   **Výchozí procento zálohy** – Zadejte částku, kterou musí zákazník zaplatit jako zálohu před tím, než může objednávku potvrdit. Výchozí minimální záloha se vypočítá jako procento z hodnoty objednávky. V závislosti na oprávněních může zaměstnanec obchodu přepsat částku pomocí možnosti **Přepsání zálohy**.
-   **Procento poplatku za zrušení** – Pokud se použije poplatek při zrušení objednávky odběratele, určete výši tohoto poplatku.
-   **Kód poplatku za zrušení** – Pokud bude použit poplatek při zrušení objednávky odběratele, tento poplatek se projeví v kódu poplatku na prodejní objednávce. Použijte tento parametr k definování kódu poplatku za zrušení.
-   **Kód dopravného** – Prodejce můžete účtovat dodatečný poplatek za dodání zboží zákazníkovi. Výše tohoto dopravného se odrazí v kódu nákladů na prodejní objednávce. Tento parametr použijte k mapování kódu dopravného na dopravné v objednávce odběratele.
-   **Refundovat dopravné** – Určete, zda je dopravné přidružené k objednávce odběratele vratné.
-   **Maximální částka bez schválení** -Pokud je dopravné vratné, určete maximální částku refundace dopravného napříč vratkami. Pokud dojde k překročení této částky, bude vyžadováno přepsání manažerem, aby bylo možné pokračovat s refundací. Pro následující scénáře může refundace dopravného překročit původně zaplacenou částku:
    -   Poplatky jsou použity na úrovni záhlaví prodejní objednávky a při vrácení určitého množství produktu nelze určit maximální refundaci dopravného povolenou pro produkty a množství takovým způsobem, který by byl použitelný pro všechny zákazníky maloobchodu.
    -   Pro každou instanci expedice vzniká dopravné. Pokud zákazník vrací produkty vícekrát a zásady prodejce určují, že prodejce ponese náklady dopravného za vrácení, budou poplatky za dopravné vratek vyšší než skutečné dopravné.

## <a name="transaction-flow-for-customer-orders"></a>Toky transakcí pro objednávky odběratele
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Vytvoření objednávky odběratele v Retail Modern POS

1.  Přidejte zákazníka do transakce
2.  Přidejte produkty do košíku.
3.  Klikněte na tlačítko **Vytvořit objednávku odběratele** a potom vyberte typ objednávky. Typ objednávky může být buď **Objednávka odběratele** nebo **Nabídka**.
4.  Klikněte na tlačítko **Odeslat vybrané** nebo **Odeslat vše** k dodání výrobků na adresu z účtu odběratele, zadejte požadované datum expedice a určete dopravné.
5.  Klikněte na tlačítko **Vyzvednout vybrané** nebo **Vyzvednout vše** pro výběr produktů, které bude být vyzvednuty z aktuálního skladu nebo jiného skladu v určité datum.
6.  Pokud je požadována záloha, vyberte částku zálohy.

### <a name="edit-an-existing-customer-order"></a>Úprava existující objednávky odběratele

1.  Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.
2.  Vyhledejte a vyberte objednávku, kterou chcete upravit. V dolní části stránky klikněte na **Upravit**.

### <a name="pick-up-an-order"></a>Vyzvednutí objednávky

1.  Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.
2.  Vyberte objednávku, která má být vyzvednuta. V dolní části stránky klikněte na **Výdej a balení**.
3.  Klikněte na **Vyzvednutí**.

### <a name="cancel-an-order"></a>Zrušení objednávky

1.  Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.
2.  Vyberte objednávku, kterou chcete zrušit. V dolní části stránky klikněte na **Zrušit**.

#### <a name="create-a-return-order"></a>Vytvořit vratku

1.  Na domovské stránce klikněte na tlačítko **Vyhledání objednávky**.
2.  Vyberte objednávku k vrácení, vyberte fakturu pro objednávku a poté vyberte produktovou řadu pro zboží k vrácení.
3.  V dolní části stránky klikněte na **Vratka**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchronní tok transakcí pro objednávky odběratele
Objednávky odběratele lze vytvořit z klienta pokladního místa buď v synchronním nebo asynchronním režimu.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Povolení vytvoření objednávky odběratele v asynchronním režimu

1.  Klikněte na **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profil POS** &gt; **Funkční profily**.
2.  Na pevné záložce **Obecné** nastavte možnost **Vytvořit objednávku odběratele v asynchronním režimu** na **Ano**.

Když je možnost **Vytvořit objednávku odběratele v asynchronním režimu** nastavena na **Ano**, objednávky odběratelů se vždy vytvářejí v asynchronním režimu, i když je k dispozici služba Retail Transaction Service. Pokud nastavíte tuto možnost na **Ne**, objednávky odběratelů jsou vždy vytvářeny v synchronním režimu pomocí služby RTS. Při vytváření objednávek odběratelů v asynchronním režimu jsou objednávky vyžádány a vloženy do aplikace Retail pomocí úloh na vyžádání (úlohy P). Odpovídající prodejní objednávky se vytvoří v aplikaci Retail buď při manuálním spuštění možnosti **Synchronizovat objednávky** nebo pomocí dávkového zpracování.

<a name="see-also"></a>Viz také
--------

[Hybridní objednávky odběratele](hybrid-customer-orders.md)




