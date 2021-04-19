---
title: Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech
description: Toto téma vysvětluje, jak nastavit vlastnosti nebezpečných materiálů pro uvolněné produkty, jak stanovit limity zásob nebezpečných položek a jak zahrnout nebezpečné materiály do prodejní objednávky, dodávky nebo nákladu.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b0fb2f77b4e95c90e3eb8a4c74929deead34de5c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829395"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit vlastnosti nebezpečných materiálů pro uvolněné produkty, jak stanovit limity zásob nebezpečných položek a jak zahrnout nebezpečné materiály do prodejní objednávky, dodávky nebo nákladu.

## <a name="set-hazardous-material-specifications-for-products"></a>Nastavení specifikací nebezpečných materiálů pro výrobky

Poté, co jste definovali regulaci nebezpečného materiálu a nastavili související referenční kódy, jak je popsáno v části [Příprava nebezpečných materiálů](hazmat-setup.md), můžete tyto informace přidružit k uvolněným položkám. Text k dodávce pro dodací doklady bude převzat z informací o nebezpečných materiálech pro uvolněné položky.

V rámci procesu přidružení uvolněné položky k nebezpečnému materiálu musíte zadat kód předpisu a materiál. K položce mohou být přidruženy různé kódy předpisů v závislosti na druzích dopravy a ke každé položce můžete přidružit více kódů předpisů a materiálů.

Chcete-li nastavit uvolněný produkt jako nebezpečný materiál, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte nebo vytvořte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.
1. Na záložce s náhledem **Spravovat sklad** nastavte možnost **Nebezpečný materiál** na **Ano**. Toto nastavení identifikuje položku jako nebezpečné zboží a použije se při tisku dokumentace expedice.
1. V podokně Akce na kartě **Spravovat sklad** ve skupině **Dodržování předpisů** vyberte **Položka nebezpečného materiálu**.
1. Vyplňte stránku **Nebezpečné materiály položky** pro vybranou položku pomocí polí, která jsou popsána v následujících podsekcích.

### <a name="item-hazardous-materials-header"></a>Záhlaví nebezpečných materiálů položky

Následující tabulka popisuje pole, která jsou k dispozici v horní části stránky **Nebezpečné materiály položky**.

| Pole | popis |
|---|---|
| Č. položky | Vydaný výrobek, se kterým pracujete. |
| Kód regulace | Vyberte nařízení o nebezpečných materiálech, které se na výrobek vztahuje. Nařízení definuje, jak se pro položku vytvoří tištěný text k dodávce a související způsoby doručení. Po přiřazení nelze kód na této stránce upravovat. Nový kód předpisu však můžete přiřadit výběrem **Nový**. |
| Kód materiálu | (Volitelně) Vyberte kód nebezpečného materiálu, který se na výrobek vztahuje. Kód materiálu poskytuje šablonu, která obsahuje výchozí hodnoty pro mnoho dalších polí na této stránce. Když vyberete kód, všechny jeho specifikace nebezpečných materiálů se zkopírují do aktuálního produktu. Systém vás však nejprve vyzve k potvrzení, že data materiálu položky by měla být vyplněna z kódu materiálu. |
| Kód skupiny | (Volitelně) Vyberte skupinu klasifikace nebezpečného materiálu, která se na výrobek vztahuje. Co se týče pole **Kód materiálu**, když vyberete kód, všechny jeho specifikace nebezpečných materiálů se zkopírují do aktuálního produktu. Systém vás však nejprve vyzve k potvrzení, že data skupiny třídy položky by měla být vyplněna z kódu skupiny. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Záložka s náhledem Popisy

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Popisy**.

| Pole | popis |
|---|---|
| Správný název expedice | Zadejte standardní popis materiálu, jak je stanoven příslušným předpisem. Překlady pro tuto hodnotu můžete poskytnout na záložce s náhledem **Překlad textu k dodávané položce**, jak je popsáno v další části. |
| Technický název | Vyberte obecný nebo obyčejný název materiálu. Tento název může být název, který vaše společnost interně používá pro materiál. |
| N.O.S. | Zaškrtnutím tohoto políčka označíte, že hodnota **Správný přepravní název** je jinak nespecifikovaný (N.O.S.) přepravní název položky. N.O.S. přepravní názvy se používají pro skupiny podobných chemikálií a materiálů, které mají konkrétní konečné použití, ale které nemusí být uvedeny podle názvu v tabulce nebezpečných materiálů ve zvláštním nařízení. |

### <a name="item-ship-text-translation-fasttab"></a>Karta s náhledem Překlad textu k dodávané položce

Karta s náhledem **Překlad textu k dodávané položce** obsahuje mřížku s překlady hodnot **Správný přepravní název**, které jsou definovány pro primární jazyk na kartě s náhledem **Popisy**. Tyto překlady lze použít v tišteném textu dodávky pro jeden nebo více jazyků.

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Překlad textu k dodávané položce**.


| Pole | popis |
|---|---|
| Jazyk | Kód jazyka, který řádek používá. Například, **pt-br** označuje brazilskou portugalštinu. |
| Tištěný text expedice | Přeložená hodnota **Správný přepravní název** v jazyce, který řádek používá. |

Chcete-li přidat nebo upravit překlad, vyberte **Překlady** nad mřížkou, čímž otevřete stránku **Překlady textu**. Potom proveďte jeden z následujících kroků:

- Chcete-li přidat nový překlad, v podokně Akce vyberte možnost **Přidat**. Vyberte jazyk, který chcete přidat, a poté v poli **Přeložený text** pole zadejte přeložený text.
- Chcete-li upravit existující překlad, vyberte cílový jazyk v poli **Jazyk** a upravte přeložený text v poli **Přeložený text** podle potřeby.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Záložka s náhledem Správa materiálu

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Správa materiálu**.

| Pole | popis |
|---|---|
| Třída | Vyberte třídu nebezpečných materiálů, do které výrobek patří, jak je definováno předpisem, kterému má vyhovovat. Každému výrobku, který obsahuje nebezpečné materiály, musíte přiřadit jak divizi, tak třídu. |
| popis | Popis, který je definován pro třídu, která je vybrána v poli **Třída**. Toto pole je určeno pouze ke čtení. |
| Divize | Vyberte divizi nebezpečných materiálů, do které výrobek patří, jak je definováno předpisem, kterému má vyhovovat. Divize je podmnožinou třídy. Každému výrobku, který obsahuje nebezpečné materiály, musíte přiřadit jak divizi, tak třídu. |
| Identifikace | Vyberte identifikační kód nebezpečného materiálu. Tento kód je obvykle založen na standardu Spojených národů (UN). |
| Skupina balení | Vyberte skupinu obalů, která platí pro aktuální položku. |
| popis | Popis, který je definován pro skupinu, která je vybrána v poli **Skupina obalů**. Toto pole je určeno pouze ke čtení. |
| Popisy balení | Vyberte příslušný kód popisu balení. Tento kód odkazuje na popis, který označuje, jak musí být produkt zabalen. |
| Popisky nebezpečných materiálů | Vyberte kód, který odkazuje na příslušný popisek nebezpečného zboží, který by měl být na výrobek použit. |
| Omezené množství | Tuto možnost nastavte na **Ano**, čímž nahlásíte celkovou hmotnost produktu, která je zahrnuta v každém nákladu a na každém řádku nákladu. |
| Množství | Zadejte množství nebezpečného materiálu ve výrobku v určených jednotkách. Tato hodnota bude použita k výpočtu celkového skóre nebezpečného materiálu pro náklady a zásilky, které obsahují produkt. |
| Multiplikátor | Zadejte násobitel, který se použije při výpočtu skóre nebezpečného materiálu pro každý řádek nákladu, který zahrnuje produkt. Tato hodnota je uvedena v příslušných předpisech podle typu nebezpečného materiálu obsaženého ve výrobku. |
| Jednotka | Vyberte měrnou jednotku, která se vztahuje na množství nebezpečného materiálu ve výrobku, jak je uvedeno v poli **Množství**. Tato hodnota bude použita k výpočtu celkového skóre nebezpečného materiálu pro náklady a zásilky, které obsahují produkt. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Jak se počítá skóre nebezpečného materiálu

Několik hodnot, které jsou uvedeny na záložce s náhledem **Správa materiálu** pro produkt se používají k výpočtu *skóre nebezpečného materiálu* pro každý řádek nákladu, který tento produkt zahrnuje. Skóre je vypočítáno pomocí následujícího vzorce:

Skóre nebezpečného materiálu = *&lt;MnožŘád&gt;* × *&lt;MnožNebMat&gt;* × *&lt;PřevodJednotek&gt;* × *&lt;Násobitel&gt;*

Zde je klíč k vzorci:

- *&lt;MnožŘád&gt;* je množství produktu, které je specifikováno pro řádek nákladu.
- *&lt;MnožNebMat&gt;* je množství nebezpečného materiálu, které je uvedeno pro produkt v poli **Množství** na záložce s náhledem **Správa materiálu**.
- *&lt;PřevodJednotek&gt;* je faktor převodu pro převod mezi jednotkou, která se používá pro množství na řádku nákladu, a jednotkou, která je uvedena pro produkt v poli **Jednotka** na záložce s náhledem **Správa materiálu**.
- *&lt;Násobitel&gt;* je násobitel, který je uveden pro produkt v poli **Násobitel** na záložce s náhledem **Správa materiálu**.

Toto skóre je hlášeno pro každý řádek nákladu, který obsahuje produkt, kde jsou uvedeny tyto hodnoty. Další informace viz [Dodávky obsahující nebezpečné materiály](#hazmat-shipments) a [Náklady obsahující nebezpečné materiály](#hazmat-loads) dále v tomto tématu.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Jak se počítá váha nebezpečného materiálu

Náklady a řádky nákladů obsahující produkty, kde je možnost **Omezené množství** na záložce s náhledem **Správa materiálu** nastavena na **Ano**, zobrazí celkovou hmotnost nebezpečného materiálu, jak je popsáno v částech [Dodávky obsahující nebezpečné materiály](#hazmat-shipments) a [Náklady obsahující nebezpečné materiály](#hazmat-loads) dále v tomto tématu. Váha nebezpečného materiálu je vypočítána pomocí následujícího vzorce:

Hmotnost nebezpečného materiálu = *&lt;MnožŘád&gt;* × *&lt;HmotnostProduktu&gt;* × *&lt;PřevodJednotek&gt;*

Zde je klíč k vzorci:

- *&lt;MnožŘád&gt;* je množství produktu, které je specifikováno pro řádek nákladu.
- *&lt;HmotnostProduktu&gt;* je čistá hmotnost specifikovaná pro produkt v měrné jednotce zásob specifikované pro produkt.
- *&lt;PřevodJednotek&gt;* je faktor převodu mezi jednotkou použitou pro množství na řádku nákladu a měrnou jednotkou zásob používané pro *&lt;Hmotnost produktu&gt;*.

### <a name="transport-information-fasttab"></a>Záložka s náhledm Informace o přepravě

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Informace o přepravě**.

| Pole | popis |
|---|---|
| Kategorie přepravy | Vyberte související kategorii přepravy. |
| Kód tunelu | Vyberte související kód pro omezení v tunelu pro položku. |
| Uskladnění nebezpečného materiálu | Vyberte referenční kód, který se používá pro manipulaci při uskladněním během námořní přepravy, když je položka zasílána námořní dopravou. |
| Typ letadla | Vyberte omezení pro letadla, které platí pro materiál dodáváný leteckou dopravou. |
| Balení - pouze nákladní letadlo | Na základě hodnoty, kterou jste vybrali v poli **Typ letadla**, vyberte kód pokynů k balení, který se použije, pokud lze produkt odeslat pouze nákladním letadlem. |
| Balení - osobní a nákladní letadla | Na základě hodnoty, kterou jste vybrali v poli **Typ letadla**, vyberte kód pokynů k balení, který se použije, pokud lze produkt odeslat buď nákladním, nebo osobním letadlem. |
| IATA Star | Tuto možnost nastavte na **Ano** k označení, že specifikace letecké dopravy, které jsou zadány na této záložce s náhledem, souvisí s normou nebezpečného zboží IATA (International Air Transport Association). Toto pole je určeno pouze pro informaci. |
| Nouzová reakce | Vyberte kód, který odkazuje na pokyny pro manipulaci s materiálem v případě nouze. |

### <a name="environmental-information-fasttab"></a>Záložka s náhledem Informace o životním prostředí

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Informace o životním prostředí**.

| Pole | popis |
|---|---|
| Nebezpečné pro životní prostředí | Tuto možnost nastavte na **Ano** k označení, že produkt je nebezpečný pro životní prostředí. Toto pole použijte pro vytváření vlastních sestav. |
| Látka znečišťující moře | Tuto možnost nastavte na **Ano** k označení, že produkt znečišťuje moře. Toto pole použijte pro vytváření vlastních sestav. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Stanovení pro omezení skladování nebezpečných výrobků

Z bezpečnostních důvodů možná budete muset omezit celkové množství daného produktu, které lze skladovat na jednom místě. Chcete-li nastavit omezení skladování pro uvolněný produkt, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt a otevřete jeho stránku **Podrobnosti o uvolněném produktu**.
1. V podokně Akce na kartě **Spravovat sklad** ve skupině **Dodržování předpisů** vyberte **Podrobnosti vytváření sestav**.
1. V polích **Omezení skladování nebezepčných materiálů** a **"Limit upozornění při skladování nebezpečných materiálů** nastavte příslušné hodnoty pro vybraný produkt.

Sestava **Omezení skladování nebezpečných materiálů** vám umožní monitorovat úrovně zásob nebezpečných materiálů ve vašich skladech, abyste se ujistili, že zůstávají pod bezpečnými limity, které jsou zde stanoveny. Další informace viz [Sestava omezení skladování nebezpečných materiálů](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Transakce prodejních objednávek, které zahrnují nebezpečné materiály

Chcete-li do prodejní objednávky zahrnout produkt klasifikovaný jako nebezpečný materiál, musíte k prodejní objednávce přidružit příslušného přepravce. Otevřete prodejní objednávku a poté na záložce s náhledem **Dodávka** nastavte dle potřeby pole **Dopravce dodávky** a **Služba dopravce**.

Přepravce je také přidružen ke způsobu doručení. Proto se musíte ujistit, že tyto informace odpovídají předpisům o nebezpečných materiálech. Jinými slovy, způsob dodání, který je uveden v nařízení o nebezpečných materiálech, musí odpovídat specifikacím v záhlaví prodejní objednávky. Tímto způsobem jsou nařízení, přepravce a služby propojeny s řádky dodávky, které jsou použity na prodejní objednávce.

Poté, co je prodejní objednávka dokončena a připravena k odeslání, může být uvolněna do skladu, čímž se označí přenos mezi prodejními a skladovými operacemi.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Dodávky, které obsahují nebezpečné materiály

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Zobrazení skóre nebezpečného materiálu pro jednotlivé řádky dodávky

Stránka **Podrobnosti o dodávce** pro dodávku zobrazuje celkovou hmotnost nebezpečného materiálu a bodové hodnoty, které byly vypočítány pro každý řádek nákladu, který je součástí dané dodávky. Chcete-li zobrazit skóre a váhy, postupujte takto.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Výběrem dodávky otevřete její stránku **Podrobnosti o dodávce**.
1. Na záložce s náhledem **Řádky nákladu** zkontrolujte řádky. U každého řádku vidíte výpočty nebezpečných materiálů v následujících polích:

    - **Body nebezpečných materiálů** – Toto pole zobrazuje skóre nebezpečného materiálu pro řádek nákladu. Hodnota se počítá podle pravidel a hodnot, které byly stanoveny pro příslušné nařízení a v nastavení uvolněného produktu. Výpočet vezme množství na řádku nákladu a odkazuje na násobitel v [nastavení správy materiálu](#material-management) pro uvolněný produkt.
    - **Čistá hmotnost omezeného množství** – U produktů, které jsou kvůli obsahu nebezpečných materiálů označeny jako produkty s omezeným množstvím, toto pole zobrazuje celkovou čistou hmotnost nebezpečného obsahu, která je uvedena na řádku nákladu. Výpočet je založen na produktech, které jsou v nastavení uvolněných produktů označeny jako nebezpečné materiály. Pokud je položka označena jako položka s omezeným množstvím, výpočet vezme množství na každém řádku nákadu a odkazuje na hmotnost v [nastavení správy materiálu](#material-management) pro uvolněný produkt.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Kontrola kompatibility mezi nebezpečnými materiály, které jsou součástí dodávky

Systém dokáže vyhodnotit, zda jsou všechny nebezpečné materiály obsažené v dodávce vhodné k tomu, aby byly odeslány společně. K vyhodnocení kompatibility systém zkontroluje skupinu kompatibility, která je přiřazena ke každému produktu, který je součástí dodávky. Další informace viz [Skupiny kompatibility nebezpečných materiálů](hazmat-setup.md#compatibility-groups).

Pokud chcete spustit kontrolu kompatibility, postupujte takto.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.
1. Výběrem dodávky otevřete její stránku **Podrobnosti o dodávce**.
1. V podokně akcí na kartě **Dodávky** ve skupině **Akce** vyberte **Kontrola kompatibility**.

Obdržíte zprávu, která vás informuje o výsledcích kontroly.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Náklady, které obsahují nebezpečné materiály

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Zobrazení skóre nebezpečného materiálu pro jednotlivé řádky nákladu

Stránka **Podrobnosti o nákladu** pro náklad zobrazuje celkovou hmotnost nebezpečného materiálu a bodové hodnoty, které byly vypočítány pro daný náklad a každý řádek nákladu. Chcete-li zobrazit skóre a váhy, postupujte takto.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny náklady**.
1. Výběrem nákladu otevřete jeho stránku **Podrobnosti o nákladu**. (Podrobnosti o nákladu můžete otevřít také výběrem odkazu ze související dodávky.)
1. Na záložce s náhledem **Náklad** můžete zkontrolovat celková skóre a váhy nebezpečného materiálu pro celý náklad kontrolou následujících polí:

    - **Body nebezpečných materiálů** – Toto pole zobrazuje skóre nebezpečného materiálu pro náklad. Hodnota se počítá podle pravidel a hodnot, které byly stanoveny pro příslušné nařízení a v nastavení uvolněného produktu. Výpočet vezme množství zahrnuté do nákladu a odkazuje na násobitel v [nastavení správy materiálu](#material-management) pro uvolněný produkt.
    - **Čistá hmotnost omezeného množství** – U produktů, které jsou kvůli obsahu nebezpečných materiálů označeny jako produkty s omezeným množstvím, toto pole zobrazuje celkovou čistou hmotnost nebezpečného obsahu, která je zahrnuta v nákladu. Výpočet je založen na produktech, které jsou v nastavení uvolněných produktů označeny jako nebezpečné materiály. Pokud je položka označena jako položka s omezeným množstvím, výpočet vezme množství v každém nákadu a odkazuje na hmotnost v [nastavení správy materiálu](#material-management) pro uvolněný produkt.

1. Chcete-li zkontrolovat skóre a váhy pro jednotlivé řádky, vyberte záložku s náhledem **Řádky nákladu**. Hodnoty zadané pro každý řádek se připomínají hodnoty zadané pro celý náklad, jak je popsáno v předchozím kroku.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Kontrola kompatibility mezi nebezpečnými materiály, které jsou součástí nákladu

Systém dokáže vyhodnotit, zda jsou všechny nebezpečné materiály obsažené v nákladu vhodné k tomu, aby byly odeslány společně. K vyhodnocení kompatibility systém zkontroluje skupinu kompatibility, která je přiřazena ke každému produktu, který je součástí nákladu. Další informace viz [Skupiny kompatibility nebezpečných materiálů](hazmat-setup.md#compatibility-groups).

Pokud chcete spustit kontrolu kompatibility, postupujte takto.

1. Přejděte na **Řízení skladu \> Dodávky \> Všechny náklady**.
1. Výběrem dodávky otevřete její stránku **Podrobnosti o nákladu**. (Podrobnosti o nákladu můžete otevřít také výběrem odkazu ze související dodávky.)
1. V podokně akcí na kartě **Náklady** ve skupině **Akce** vyberte **Kontrola kompatibility**.

Obdržíte zprávu, která vás informuje o výsledcích kontroly.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]