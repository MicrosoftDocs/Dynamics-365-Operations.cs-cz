---
title: Snížení hodnoty používaného majetku
description: Toto téma popisuje funkci, která zaznamenává snížení hodnoty a upravuje plán odpisů majetku u operativního leasingu s tématem Kodifikace účetních standardů 842 (ASC 842).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9822a11dbb277726b60ff82843bd26314e968345
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003249"
---
# <a name="impair-right-of-use-assets"></a>Snížení hodnoty používaného majetku

[!include [banner](../includes/banner.md)]

Pokud není zůstatková hodnota používaného majetku (ROU) zpětně získatelná, možná budete muset otestovat, zda je snížena hodnota daného majetku. Pokud zjistíte, že došlo ke snížení hodnoty aktiva, může leasing aktiv zaznamenat snížení hodnoty a odpovídajícím způsobem upravit odpisový plán. Toto téma popisuje funkci, která zaznamenává snížení hodnoty a upravuje plán odpisů u operativního leasingu s tématem Kodifikace účetních standardů 842 (ASC 842). Stejná metoda platí i pro leasingy podle mezinárodního standardu Financial Reporting 16 (IFRS 16).

Zbývající zůstatek používaného majetku bude odepisován rovnoměrně po dobu zbývajících období, bez ohledu na to, zda byl leasing klasifikován jako finanční leasing podle IFRS 16 nebo operativní leasing podle ASC 842.

## <a name="impair-an-rou-asset"></a>Snížení hodnoty majetku ROU

1. Přejděte na leasing se sníženou hodnotou a vyberte **Knihy**.
2. V podokně akcí vyberte **Snížení hodnoty**.
3. V dialogovém okně, které se zobrazí, do pole **Snížení hodnoty** zadejte částku snížení hodnoty majetku. Chcete-li snížit hodnotu používaného majetku, měli byste zadat kladnou hodnotu.
4. Do pole **Datum transakce** zadejte datum, kdy má být položka snížení hodnoty zaúčtována.
5. Do pole **Zbývající období** zadejte zbývající počet měsíců k amortizaci.
6. Zapněte parametr **Zaúčtovat**, pokud chcete, aby systém automaticky zaúčtoval položku deníku výdajů pro snížení hodnoty. Pokud necháte tento parametr vypnutý, systém vytvoří záznam, ale nezaúčtuje jej. Poté můžete příspěvek zaúčtovat na straně **Deníky o pronájmu majetku**.
7. Nastavte možnost **Náhled před zaúčtováním** na **Ano**, chcete-li zobrazit navrhovanou položku před jejím vytvořením nebo zaúčtováním.
8. Nastavte možnost **Zavřít knihu** na **Ano**, chcete-li uzavřít knihu pronájmu. Tuto akci nelze vrátit zpět. Záznamy nelze zaúčtovat proti uzavřeným leasingům a uzavřené leasingy nelze upravovat.
9. Vyberte **OK**, chcete-li vytvořit nebo zaúčtovat položku snížení hodnoty.
10. Chcete-li zobrazit plán odpisů aktiv se sníženou hodnotou, otevřete plán odpisů aktiv pro danou leasingovou knihu. Majetek bude nyní odepisován rovnoměrně po dobu měsíců, které jste zadali v poli **Zbývající období**.
11. Chcete-li zobrazit položku deníku výdajů na snížení hodnoty, vyberte **Deník leasingu majetku** v podokně akcí knihy pronájmu se sníženou hodnotou. Systém vytvoří zápis do deníku, který debituje účet zaúčtování výdajů na snížení hodnoty a kredituje účet zaúčtování majetku leasingu.
12. Chcete-li zobrazit novou účetní hodnotu používaného majetku, vyberte **Transakce majetku** v podokně akcí knihy pronájmu.

## <a name="example-of-rou-asset-impairment"></a>Příklad snížení hodnoty používaného majetku

V tomto příkladu se jedná o pronájem nespecializovaného majetku, který nepřenáší vlastnictví ani neposkytuje nájemci možnost nákupu.

### <a name="setup"></a>Nastavení

Následující tabulky ukazují hodnoty, které jsou nastaveny na kasrtách **Všeobecné** a **Řádky platebního plánu** pro pronájem použitý v tomto příkladu.

**Karta Obecné**

| Pole                      | Hodnota            |
|----------------------------|------------------|
| Reálná hodnota majetku    | 600,000          |
| Přírůstková výpůjční úroková sazba | 7%               |
| Interval úročení       | Ročně         |
| Očekávaná doba použitelnosti majetku (měsíce) | 600              |
| Typ anuity               | Běžná anuita |
| Datum zahájení          | 01/01/2019       |

**Karta Řádky platebního kalendáře**

| Pole             | Hodnota      |
|-------------------|------------|
| Počáteční datum        | 1/1/2019   |
| Interval období   | Měsíčně    |
| Období           | 120        |
| Koncové datum          | 12/31/2028 |
| Četnost plateb | Ročně   |
| Částka platby    | 10,000     |

### <a name="steps"></a>Kroky

1. Po vytvoření pronájmu, jak je popsáno výše v tomto tématu, přejděte do knihy pronájmů a potvrďte plán plateb. Poté zaúčtujte počáteční uznání do deníku. Počáteční používaný majetek a leasingový závazek by měl být 70 235,81 USD. V tomto příkladu byl leasing klasifikován jako operativní leasing podle ASC 842.
2. Spusťte proces dávkového deníku třikrát, abyste simulovali průběh tří let pro leasingové splátky, úrokové výdaje a odpisy.
3. Po dokončení spuštění všech tří dávkových úloh se vraťte zpět do knihy pronájmů a otevřete tabulky závazků a transakcí aktiv, abyste zobrazili aktuální účetní hodnotu používaného majetku a leasingového závazku. Po třech letech by hodnota závazku měla být přibližně -53 893,00 USD a hodnota aktiva by měla být přibližně 53 893,00 USD. 

    Po třech letech podnik provede testy na snížení hodnoty a zjistí, že používaný majetek má sníženou hodnotu o 35 000 USD. Nyní musíte toto snížení hodnoty zaznamenat.
    
4. Přejděte do knihy pronájmů a poté v podokně akcí vyberte **Snížení hodnoty**.
5. Na stránce **Parametr snížení hodnoty** zadejte následující podrobnosti.

    | Pole                  | Hodnota    |
    |------------------------|----------|
    | Částka snížení hodnoty      | 35,000   |
    | Datum transakce       | 1/1/2022 |
    | Zbývající období      | 84       |
    | Zaúčtovat                   | Ano      |
    | Náhled před zaúčtováním | Žádný       |
    | Uzavřít knihu             | Žádný       |

6. Byla vytvořena a zaúčtována položka deníku výdajů na snížení hodnoty. Chcete-li ji zobrazit, přejděte do deníku leasingu majetku v leasingové knize. Všimněte si, že částka snížení hodnoty byla odepsána z účtu zaúčtování nákladů na snížení hodnoty a byla připsán na účet zaúčtování používaného majetku.
7. Čistý dopad snížení hodnoty zobrazíte v tabulkách transakcí s aktivy a pasivy. Všimněte si, že snížení hodnoty snížilo používaný majetek, ale účetní hodnota leasingového závazku se nezměnila.

Snížení hodnoty má ještě jeden další účinek, který byste měli zvážit. Protože částka používaného majetku je nyní mnohem menší než závazek z leasingu, částka musí být odepsána jinak, než tomu bylo dříve. Konkrétně je majetek nyní odepisován rovnoměrně po zbývajících 84 měsíců leasingu, počínaje dnem transakce.
