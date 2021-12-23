---
title: Nastavení daňových kódů
description: Toto téma vysvětluje, jak nastavit daňové kódy ve službě výpočtu daně.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883846"
---
# <a name="set-up-tax-codes"></a>Nastavení daňových kódů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit daňové kódy ve službě výpočtu daně. Zahrnuje nastavení pro jednoduchý scénář, který zajistí funkčnost daňového kódu, a informace o některých pokročilých funkcích daňového kódu pro složité scénáře.

> [!IMPORTANT]
> Nastavení daňových kódů ve službě výpočtu daně nerozlišuje právnické osoby. Toto nastavení můžete ve službě Regulatory Configuration Service (RCS) provést pouze jednou. Daňové kódy se automaticky synchronizují se Microsoft Dynamics 365 Finance, když ve Finance povolíte službu výpočtu daně pro vybranou právnickou osobu.

## <a name="simple-setup"></a>Jednoduché nastavení

Chcete-li použít daňový kód v jednoduchém scénáři, například když existuje pouze jedna sazba daně, postupujte podle těchto kroků.

1. Přihlaste se ke službě [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Jdětena **Pracovní prostory** \> **Funkce globaliizace** \> **Výpočet daně**.
3. Vyberte funkci a verzi, kterou chcete nastavit, a vyberte **Upravit**.
4. Na kartě **Obecné** vyberte **Verze konfigurace**.
5. Na kartě **Daňové kódy** vyberte **Přidat** a zadejte daňový kód a popis.
6. Vyberte možnost **Původ výpočtu**. Původ výpočtu je skupina metod, které jsou definovány ve vybrané verzi konfigurace daně. Pro tento jednoduchý scénář vyberte **Podle čisté částky**.
7. Zvolte možnost **Uložit**. Na základě vybraného původu výpočtu se zpřístupní více polí.
8. Na záložce s náhledem **Sazby** volbou **Přidat** přidáte jednu sazbu daně pro tento daňový kód.
9. Zvolte možnost **Uložit**.

## <a name="calculation-origin"></a>Původ výpočtu

Původ výpočtu definuje, jak se vypočítá částka základu daně a částka daně. Je konfigurován pomocí konfigurace daně v pracovním prostoru **Elektronické výkaznictví**. Následující hodnoty jsou k dispozici v poli **Původ konfigurace**:

- Podle čisté částky
- Podle hrubé částky
- Podle množství
- Podle marže
- Daň z daně

### <a name="by-net-amount"></a>Podle čisté částky

Pokud vyberete **Podle čisté částky** v poli **Původ výpočtu**, částka daně se vypočítá jako procento z částky nákupu nebo prodeje bez jakýchkoli jiných daňových kódů.

Například sazba daně je 25 procent, řádek faktury zobrazuje množství 10 položek po 1,00 a zákazníkovi je povolena sleva na řádku 10 procent. V tomto případě jsou částky vypočteny následujícím způsobem:

- **Čistá částka:** (10 × 1,00) – 10 procent = 9,00 
- **Prodejní daň:** 9,00 × 25 procent = 2,25 
- **Celková fakturovaná částka:** = 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Podle hrubé částky

Pokud vyberete **Podle čisté částky** v poli **Původ výpočtu**, částka daně je vypočtena jako procento z hrubé prodejní částky. Hrubá částka je čistá částka na řádku plus všechny daně a poplatky pro řádek kromě jedné daně, kde je pole **Původ zdroje** je nastavno na **Podle hrubé částky**.

Například daňový úřad na položku uložil zvláštní cla. Částky cla se před výpočtem daně přičtou k čisté částce. Jsou použity následující daňové kódy:

- **Clo 1** – Sazba je 10 procent a je použita metoda výpočtu **Podle čisté částky**.
- **Clo 2** – Sazba je 20 procent a je použita metoda výpočtu **Podle čisté částky**.
- **Dazba daně** – Sazba je 25 procent a je použita metoda výpočtu **Podle hrubé částky**.

Pokud je čistá částka 10,00, částka cla 1 je 1,00 (10,00 × 10 procent) a částka cla 2 je 2,00 (10,00 × 20 procent). V tomto případě jsou částky vypočteny následujícím způsobem: 

- **Hrubá částka:** Čistá částka + částka cla 1 + částka cla 2 = 10,00 + 1,00 + 2,00 = 13,00 
- **Částka daně:** 13,00 × 25 procent = 3,25 
- **Celková cla a daně:** 1,00 + 2,00 + 3,25 = 6,25 
- **Celková fakturovaná částka:** = 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Podle množství

Vyberete-li **Podle množství** v poli **Původní výpočet** se částka daně vypočítá jako pevná částka za jednotku vynásobená množstvím zadaným na řádku dokladu. Částka za jednotku je uvedena na záložce s náhledem **Sazby**.

Například daňový kód je nastaven na 1,20 za jednotku. Na řádku prodejní faktury je prodáno 25 jednotek položky. V tomto případě je částka daně vypočítána jako 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Podle marže

Pokud vyberete **Podle marže** v poli **Původ výpočtu**, částka daně je vypočtena jako procento z prodejní marže. Prodejní marže je částka prodeje mínus částka nákladů. Tento způsob výpočtu se vztahuje pouze na prodejní transakce.

Například sazba daně je 25 procent, řádek faktury zobrazuje množství 10 položek po 10,00 a náklady na položku jsou 6. V tomto případě jsou částky vypočteny následujícím způsobem:

- **Prodejní marže:** 10 × ( 10,00 – 6,00) = 40,00
- **Částka daně:** 40,00 × 25 procent = 10,00
- **Celková fakturovaná částka:** = 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Daň z daně

Pokud vyberete **Daň z daně** v poli **Původ výpočtu**, DPH je vypočítáno jako procento ze všech ostatních částek daně na stejném řádku dokladu.

Například jsou použity následující daňové kódy:

- **Clo 1** – Sazba je 10 procent a je použita metoda výpočtu **Podle čisté částky**.
- **Clo 2** – Sazba je 20 procent a je použita metoda výpočtu **Podle čisté částky**.
- **Daň ze cla** – Sazba je 25 procent a je použita metoda výpočtu **Daň z daně**.

V tomto případě jsou částky vypočteny následujícím způsobem:

- **Čistá částka**: 10,00 
- **Clo 1:** 10,00 × 10 procent = 1,00 
- **Clo 2:** 10,00 × 20 procent = 2,00 
- **Daň ze cla:** 3,00 × 25 procent = 0,75
- **Celková daň:** 1,00 + 2,00 + 0,75 = 3,75 
- **Celková fakturovaná částka:** = 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Rozšířená funkce

Tato část vysvětluje některé rozšířené funkce nastavení daňového kódu pro složité scénáře.

### <a name="tax-exemption"></a>Osvobození od daně

Pokud nastavíte možnost **Je osvobozeno od daně** na **Ano** na záložce s náhledem **Obecné**, částka daně bude vždy přepsána na 0 (nula) bez ohledu na skutečnou sazbu daně.

Pole **Kód osvobození od daně** můžete nastavit, abyste zadali důvod osvobození od daně. 

Můžete povolit vyhledávání hlavních dat pro pole **Kód osvobození od daně**. Tímto způsobem si můžete vybrat mezi hodnotami kódu osvobození od daně, které jsou definovány ve Finance. Informace o tom, jak povolit vyhledávání hlavních dat, viz [Povolení vyhledávání hlavních dat pro konfiguraci výpočtu daně](tax-service-set-up-environment-master-data-lookup.md).

Například sazba daně je 25 procent a možnost **Je osvobozeno od daně** je nastavena na **Ano** pro daňový kód. Řádek faktury zobrazuje množství 10 položek po 1,00 za kus a odběrateli je poskytnuta 10procentní řádková sleva. V tomto případě jsou částky vypočteny následujícím způsobem:

- **Čistá částka:** (10 × 1,00) – 10 procent = 9,00 
- **DPH:** 0,00 
- **Celková fakturovaná částka:** = 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Importní DPH

Pokud nastavíte možnost **Je importní DPH** na **Ano** na záložce s náhledem **Obecné**, částka daně bude zaúčtována do účtu **Splatná importní DPH** místo účtu **Souhrn dodavatele**.

Například sazba daně je 25 procent a možnost **Je importní DPH** je nastavena na **Ano** pro daňový kód. Řádek faktury zobrazuje množství 10 položek po 1,00 za kus a odběrateli je poskytnuta 10procentní řádková sleva. V tomto případě jsou částky vypočteny následujícím způsobem:

- **Čistá částka:** (10 × 1,00) – 10 procent = 9,00 
- **Importní DPH:** 9,00 × 25 procent = 2,25
- **Celková fakturovaná částka:** = 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Pokud jsou obě možnosti **Je osvobozeno od daně** a **Je importní DPH** nastaveny na **Ano** u daňového kódu, kód bude uznán jako osvobozený od daně pro prodejní transakce a importní DPH pro nákupní transakce.

### <a name="reverse-charges"></a>Stornovací poplatky

Pokud nastavíte možnost **Je přenesení daňové povinnosti** na **Ano** na záložce s náhledem **Obecné**, daňovou sazbu lze nakonfigurovat jako zápornou. Pro scénář přenesení daňové povinnosti doporučujeme nastavit dva daňové kódy: jeden má kladnou sazbu daně a jeden má zápornou sazbu daně. Oba daňové kódy by měly mít stejnou hodnotu sazby a možnost **Je přenesení daňové povinnosti** by měla být nastavena na **Ano** u daňového kódu, který má zápornou daňovou sazbu. Další informace o řešení přenesení daňové povinnosti ve Finance najdete v části [Mechanismus přenesení daňové povinnosti pro režim DPH / GST](emea-reverse-charge.md).

Na jednom řádku faktury jsou například určeny dva daňové kódy. Jedna sazba daně je 25 procent. Další sazba daně je −25 procent a možnost **Je přenesení daňové povinnosti** je nastavena na **Ano** pro druhý daňový kód. Řádek faktury zobrazuje množství 10 položek po 1,00. V tomto případě jsou částky vypočteny následujícím způsobem:

- **Čistá částka:** (10 × 1,00) = 10,00 
- **Daňový kód 1:** 10,00 × 25 procent = 2,50
- **Daňový kód 2:** 10 × −25 procent = −2,50
- **Celková fakturovaná částka:** 10,00 + 2,50 −2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Vyloučení z výpočtů základní částky

Pokud nastavíte možnost **Vyloučit z výpočtu základní částky** na **Ano** na záložce s náhledem **Obecné**, vypočtená částka daně kódu daně je vyloučena z částky základu daně pro ostatní výpočty kódu daně ve scénáři zahrnujícím cenu.

Další informace viz [Výpočet daně u cen, když jsou povoleny ceny včetně daní](global-exclude-from-tax-base-amount-calculation.md).

### <a name="rates"></a>Sazby

Na záložce s náhledem **Sazba** můžete definovat různé daňové sazby pro různé rozsahy částek základu daně. Pro výpočet výše daně služba výpočtu daně vždy používá sazbu, která odpovídá částce základu daně.

Například daňové sazby mohou být nakonfigurovány tak, jak je uvedeno v následující tabulce.

| Minimální částka | Maximální množství | Sazba daně   |
| -------------- | -------------- | ---------- |
| 0              | 1 000          | 10 procent |
| 1 000          | 5 000          | 15 procent |
| 5 000          | 10,000         | 20 procent |
| 10,000         | 0              | 30 procent |

V tomto případě je částka daně vypočtena následujícím způsobem:

- Je-li částka základu daně 300,00, sazba daně je 10 procent a částka daně je 300,00 × 10 procent = 30,00.
- Je-li částka základu daně 3 000,00, sazba daně je 15 procent a částka daně je 3 000,00 × 15 procent = 450,00.
- Je-li částka základu daně 6 000,00, sazba daně je 20 procent a částka daně je 6 000,00 × 10 procent = 1 200,00.
- Je-li částka základu daně 20 000,00, sazba daně je 30 procent a částka daně je 20 000,00 × 30 procent = 6 000,00.

> [!NOTE]
> Pokud se částka základu daně může shodovat jak s maximální částkou na jednom řádku, tak s minimální částkou na druhém řádku, základ použije sazbu daně, která odpovídá minimální částce základu. Například je-li částka základu daně 1000,00, sazba daně je 15 procent a částka daně je 1 000,00 × 15 procent = 150,00.

### <a name="limits"></a>Limity

Na záložce s náhledem **Omezení** můžete definovat omezení daní, která přepíší vypočtenou částku daně, pokud částka daně spadá do minimálního/maximálního rozsahu.

- Pokud je vypočtená částka daně větší nebo rovna maximální částce daně, která je nakonfigurována na záložce s náhledem **Omezení**, konečná částka daně se rovná maximální částce daně.
- Pokud je vypočtená částka daně nižší než minimální částka daně, která je nakonfigurována na záložce s náhledem **Omezení**, konečná částka daně je 0 (nula).

Například omezení daní jsou konfigurována následujícím způsobem:

- **Minimální částka daně:** 100 
- **Maximální částka daně:** 1 000

Pokud je vypočtená částka daně 2 000, konečná částka daně je 1 000.

Pokud je vypočtená částka daně 500, konečná částka daně je 500.

Pokud je vypočtená částka daně 80, konečná částka daně je 0 (nula).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
