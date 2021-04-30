---
title: Návrh ukončení leasingu
description: Toto téma vysvětluje, jak navrhnout ukončení leasingu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b32f9e8f80827e04269ac8cb6a4fbb5a13af8bc
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881101"
---
# <a name="propose-a-lease-for-termination"></a>Navrhnout ukončení leasingu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pokud je leasing ukončen předčasně, leasing majetku může vytvořit záznam deníku ukončení, aby odepsal závazek z leasingu, používaný majretek (ROU) a akumulované odpisy a zaúčtoval zisk nebo ztrátu. Proces předčasného ukončení ukončí leasing a související přidružené leasingové knihy. Neukončí jednotlivé leasingové knihy. Toto téma popisuje funkce, které vám umožňují navrhnout ukončení leasingu a zpracovat položku deníku ukončení leasingu.

Pokud leasing není klasifikován jako leasing s odloženými splátkami a není spojen s dlouhodobým majektem, leasing majetku vytvoří následující položku deníku ukončení.

| Transakce                           | Má dáti (MD) | Dal (D) |
|---------------------------------------|-------------|--------------|
| MD Leasingový závazek                   | X           |              |
| MD akumulovaný odpis          | X           |              |
| MD Zisk (ztráta) při upravení leasingu | X           |              |
| D Aktivum leasingu                       |             | X            |
| D Zisk (ztráta) při upravení leasingu |             | X            |

Pokud je leasingová kniha klasifikována jako kniha odložených splátek, položka odepíše zůstatek odloženého nájemného před ukončením na účet zisků nebo ztrát, jak je znázorněno zde.

| Transakce                           | Má dáti (MD) | Dal (D) | 
|---------------------------------------|-------------|--------------|
| MD Odložená splátka                     | X           |              |
| D Zisk (ztráta) při upravení leasingu |             | X            |
| D Odložená splátka                     |             | X            |
| MD Zisk (ztráta) při upravení leasingu | X           |              |

Pokud je leasingová kniha připojena k dlouhodobému majetku, používaný majetek se účtuje v položce dlouhodobý majetek. Toto účetnictví zahrnuje účtování předčasného ukončení. Leasing aktiv vytvoří následující zápis do deníku k odpisu závazku z leasingu.

| Transakce                           | Má dáti (MD) | Dal (D) |
|---------------------------------------|-------------|--------------|
| MD Leasingový závazek                   | X           |              |
| D Zisk (ztráta) při upravení leasingu |             | X            |

Informace o správné likvidaci používaného majetkku viz [Likvidace dlouhodobého majetku jako odpad](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Navrhnout ukončení leasingu

1. Přejděte na leasing, který musí být ukončen, a poté v podokně akcí vyberte **Návrh na ukončení**.

    > [!NOTE]
    > Tlačítko **Návrh na ukončení** není k dispozici, pokud existují nějaké nezaúčtované položky deníku u jakékoli knihy. Než budete moci ukončit leasing, musíte zaúčtovat nebo odstranit všechny položky deníku, které byly vytvořeny proti leasingu.

2. V zobrazeném dialogovém okně nastavte pole **Datum platnosti** a **Datum zaúčtování** pole pro položku deníku ukončení.
3. Vyberte **Návrh na ukončení**, chcete-li navrhnout ukončení leasingu.
4. Vyberte **Zaúčtovat ukončení leasingu**, chcete-li automaticky zaúčtovat položku deníku ukončení leasingu.
5. Na stránce **Ukončení leasingu** vyberte ID leasingu, který jste navrhli pro ukončení, abyste zobrazili řádky ukončení. Řádky ukončení zobrazují účetní hodnoty používaného majetku, závazku z leasingu, akumulovaných odpisů, odložených splátek (je-li relevantní) a zisku nebo ztráty, které musí být vykázány při ukončení leasingu.

Leasing je nyní připraven k ukončení. Hodnota pole **Stav ukončení** pro leasingovou knihu se změní na **Připraveno k ukončení**. V tomto okamžiku již nemůžete zaúčtovat položky deníku proti leasingu nebo jej upravit nebo snížit hodnotu. 

## <a name="process-leases-that-are-ready-for-termination"></a>Zpracujte leasingy, které jsou připraveny k ukončení

Chcete-li zpracovat leasingy, které jsou připraveny k ukončení, a zaúčtovat položku deníku ukončení, postupujte takto.

1. Na stránce **Ukončení leasingu** vyberte leasing, který chcete zpracovat, a poté vyberte **Ukončit**.
2. V zobrazeném dialogovém okně vyberte **OK**.

Systém zaúčtuje položku deníku ukončení. Pole **Stav leasingu** pro leasigovou knihu je nastaveno na **Ukončeno** a pole **Stav návrhu na ukončení** je nastaveno na **Dokončeno**.

## <a name="reverse-a-lease-termination"></a>Storno ukončení leasingu

Chcete-li stornovat položku deníku ukončení leasingu a otevřít ukončený leasing, postupujte takto.

- Na stránce **Ukončení leasingu** vyberte ukončený leasing, který chcete stornovat, a poté vyberte **Storno ukončení**.

Systém stornuje položku deníku ukončení. Pole **Stav leasingu** pro leasingovou knihu je nastaveno na **Otevřeno**. Leasing se již nezobrazuje na stránce **Ukončení leasingu** a lze jej znovu navrhnout k ukončení.

## <a name="example-of-a-lease-termination"></a>Příklad ukončení leasingu

V tomto příkladu je leasing spojený s nespecializovaným majetkem a nepřenáší vlastnictví majetku ani neposkytuje nájemci možnost jeho nákupu.

### <a name="setup"></a>Nastavení

Následující tabulky ukazují hodnoty, které jsou nastaveny na kasrtách **Všeobecné** a **Řádky platebního plánu** pro pronájem použitý v tomto příkladu.

**Karta Obecné**

| Pole                      | Hodnota            |
|----------------------------|------------------|
| Reálná hodnota majetku    | 600,000          |
| Měna                   | USD              |
| Počáteční přímé náklady       | 1 000            |
| Přírůstková výpůjční úroková sazba | 7%               |
| Interval úročení       | Ročně         |
| Očekávaná doba použitelnosti majetku (měsíce) | 600              |
| Typ anuity               | Běžná anuita |
| Datum zahájení          | 1/1/2019         |

**Karta Řádky platebního kalendáře**

| Pole             | Hodnota      |
|-------------------|------------|
| Počáteční datum        | 1/1/2019   |
| Interval období   | Měsíčně    |
| Období           | 120        |
| Koncové datum          | 12/31/2028 |
| Četnost plateb | Ročně   |
| Částka platby    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Kroky pro ukončení leasingu

1. Po vytvoření pronájmu, jak je popsáno výše v tomto tématu, přejděte do knihy pronájmů a potvrďte plán plateb. Poté zaúčtujte počáteční uznání do deníku. Počáteční používaný majetek má hodnotu 71 235,81 USD a leasingový závazek by měl být 70 235,81 USD. V tomto příkladu byl leasing klasifikován jako operativní leasing podle Tématu kodifikace účetních standardů 842 (ASC 842).
2. Spusťte proces dávkového deníku třikrát, abyste simulovali průběh tří let pro leasingové splátky, úrokové výdaje a odpisy.
3. Po dokončení spuštění všech tří dávkových úloh se vraťte zpět do leasingové knihy a otevřete tabulky transakcí s aktivy a pasivy, abyste zobrazili aktuální účetní hodnotu používaného majetku a leasingových závazků. Po třech letech by hodnota pasiv měla být přibližně -53 893,00 USD a hodnota aktiv by měla být přibližně 54 593,00 USD.

    Po uplynutí tří let se podnikatel a pronajímatel vzájemně dohodnou na ukončení leasingu. Proto nyní musíte leasing ukončit.

4. Přejděte na leasing, který musí být ukončen, a poté v podokně akcí vyberte **Návrh na ukončení**. 
5. V dialogovém okně, které se zobrazí, v poli **Datum platnosti** a **Datum zaúčtování** zadejte **1/1/2021**.
6. Vyberte **Návrh na ukončení**, chcete-li navrhnout ukončení leasingu.

    Zobrazí se stránka **Ukončení leasingu** s leasingem, který bude ukončen.

7. Chcete-li zobrazit řádky ukončení, vyberte ID leasingu, který jste navrhli pro ukončení. Řádky ukončení ukazují účetní hodnoty leasingu. Následující tabulka ukazuje, jaké by měly být tyto hodnoty pro tento příklad. 

    | Pole                                                 | Hodnota      |
    |-------------------------------------------------------|------------|
    | Účetní zůstatek závazků v měně transakce | 53 892,89 USD |
    | Používaný majetek v měně transakce            | 71 235,81 USD |
    | Akumulované odpisy v měně transakce      | 16 642,92 USD |
    | Zisk (ztráta) v měně transakce                   | -700,00 USD   |

8. Chcete-li zaúčtovat položku deníku ukončení, na stránce **Ukončení leasingu** vyberte leasing a poté vyberte **Ukončit**.
9. V zobrazeném dialogovém okně vyberte **OK**.
10. Chcete-li zobrazit položku deníku ukončení, který byl vytvořen a zaúčtován, přejděte do deníku leasingu majetku v leasingové knize. Následující tabulka ukazuje, jak by měla tato položka vypadat pro tento příklad.

    | Transakce                           | Má dáti (MD) | Dal (D) |
    |---------------------------------------|-------------|--------------|
    | MD Leasingový závazek                   | 53,892.89   |              |
    | MD akumulovaný odpis          | 16,642.92   |              |
    | MD Zisk (ztráta) při upravení leasingu | 700.00      |              |
    | D Aktivum leasingu                       |             | 71,235.81    |

11. Chcete-li zobrazit čistý efekt ukončení, kde používaný majetek a závazek z leasingu budou 0 (nula), otevřete tabulky transakcí a aktivy a pasivy.

Stav leasingu by nyní měl být **Ukončeno**. Proti tomuto leasingu nebudou zaúčtovány žádné další položky deníku, pokud nebude ukončení stornováno.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
