---
title: Operace vyhledání zásob v POS
description: Toto téma popisuje, jak použít operaci vyhledávání zásob v pokladním místě (POS) Dynamics 365 Commerce pro zobrazení dostupnosti skladových zásob produktů v obchodech a skladech.
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: c0f753febb0d347015fde1374148835f90df55a3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353773"
---
# <a name="inventory-lookup-operation-in-pos"></a>Operace vyhledání zásob v POS

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak použít operaci vyhledávání zásob v pokladním místě (POS) Dynamics 365 Commerce pro zobrazení dostupnosti skladových zásob produktů v obchodech a skladech.

Přesné zobrazení zásob napříč organizací pomáhá zaměstnancům obchodu poskytovat včasný a efektivní zákaznický servis. Nejdůležitějším okamžikem je okamžik, kdy je zákazník připraven k rozhodnutí o koupi. Je důležité, aby pokladníci v obchodě měli k dispozici informace o zásobách v reálném čase, aby mohli přesně zaručit dodání a vyzvednutí produktu.

Operace vyhledávání zásob v Commerce POS pomáhá maloobchodníkům dosáhnout provozní dokonalosti a získat přehled propojením obchodů s centrálou Commerce. Tato funkce poskytuje pohled na dostupnost zásob produktů v obchodech a skladech. Rovněž pomáhá maloobchodním prodejcům využít další efektivní možnosti a úspory nákladů díky zlepšenému plánování zásob v reálném čase.

Když je operace vyhledávání zásob spuštěna z aplikace POS, pokladník POS používá numerickou klávesnici k zadání čísla produktu k dotazu na informace o zásobách. Pokud má zadaný produkt varianty, může pokladník volitelně vybrat dimenze nebo jiné hodnoty a zkontrolovat informace o zásobách konkrétní varianty produktu.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Zobrazení vyhledávacího seznamu zásob pro jednotlivé produkty

Pro jednotlivý produkt poskytuje operace vyhledávání zásob zobrazení seznamu vyhledávání zásob zobrazující následující informace o produktu pro seznam umístění:

- **Zásoby** - Odkazuje na „dostupné fyzické“ množství produktu.
- **Rezervováno** - Odkazuje na „fyzické rezervované“ množství načtené z ústředí.
- **Objednané** - Odkazuje na „objednané celkové“ množství načtené z ústředí.
- **Jednotka** - Odkazuje na měrnou jednotku zásob nakonfigurovanou v ústředí.

Zobrazení seznamu umístění zahrnuje všechny obchody a sklady, které jsou konfigurovány ve skupinách plnění, s nimiž je propojen aktuální obchod, jak je znázorněno na následujícím vzorovém obrázku.

![Zobrazení seznamu operace vyhledání zásob.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Ujistěte se, že je váš aktuální obchod zahrnut do přidružených skupin plnění.

Na panelu aplikací POS jsou k dispozici následující akce:

- **Seřadit** - Tato akce umožňuje uživateli POS seřadit data v zobrazení seznamu na základě různých kritérií. Třídění podle umístění je výchozí možností řazení. 
  - **Geografická poloha** (od nejbližšího místa po nejvzdálenější místo ve srovnání s aktuálním obchodem)
  - **Název** (ve vzestupném nebo sestupném pořadí)
  - **Číslo ve skladu** (ve vzestupném nebo sestupném pořadí)
  - **Zásoby** (v sestupném pořadí)
  - **Rezervované** (v sestupném pořadí)
  - **Objednané** (v sestupném pořadí)
- **Filtr** - Tato akce umožňuje uživateli POS prohlížet filtrovaná data pro konkrétní umístění.
- **Zobrazit dostupnost obchodu** - Tato akce umožňuje uživateli POS zobrazit dostupné množství (ATP) pro produkt ve vybraném obchodě.
- **Zobrazit umístění obchodu** - Tato akce otevře samostatnou stránku pro zobrazení zobrazení mapy, adresy a otevírací doby vybraného obchodu.
- **Vyzvednout v obchodě** - Tato akce vytvoří objednávku zákazníka pro variantu produktu, která bude vyzvednuta z vybraného obchodu, a přesměruje uživatele na obrazovku transakce.
- **Expedovat produkt** - Tato akce vytvoří objednávku zákazníka pro variantu produktu, která bude expedována z vybraného obchodu, a přesměruje uživatele na obrazovku transakce.
- **Zobrazit všechny varianty** - U produktu s variantami se tato akce přepne ze zobrazení seznamu do zobrazení matice, které zobrazí informace o zásobách pro všechny varianty produktu.
- **Přidat k transakci** - Tato akce přidá produkt do košíku a přesměruje uživatele na obrazovku transakce.

> [!NOTE]
> U řazení založeného na umístění je vzdálenost mezi místem a aktuálním úložištěm určena souřadnicemi (zeměpisná šířka a délka) definované v obchodním ústředí. U úložiště jsou informace o poloze definovány na primární adrese provozní jednotky spojené s úložištěm. U skladu, který není skladem, jsou informace o umístění definovány v adrese skladu. Pokud aktuální úložiště nemá definované souřadnice, zobrazí možnost řazení podle umístění aktuální úložiště v horní části seznamu a poté seřadí další umístění podle názvu.

> [!NOTE]
> Akce **Zobrazit dostupnost obchodu**, **Zobrazit umístění obchodu**, **Vyzvednout v obchodě** a **Odeslat produkt** nejsou k dispozici pro umístění mimo prodejnu.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Zobrazení matice vyhledávání zásob pro varianty

U hlavního produktu s variantami poskytuje operace vyhledávání zásob také maticové zobrazení založené na dimenzích, které zobrazuje informace o dostupnosti zásob pro všechny varianty hlavního produktu na vybraném místě. Ve výchozím nastavení maticové zobrazení ukazuje data pro aktuální prodejnu. Můžete použít akci **Obchod** na panelu aplikací k vyhledání informací o zásobách v jiných obchodech nakonfigurovaných ve skupinách plnění, ke kterým je aktuální obchod připojen.

Následující ukázkový obrázek ukazuje zobrazení matice vyhledávání zásob v POS.

![Maticové zobrazení operace vyhledání zásob.](media/inventory-lookup-matrix-view.png)

V maticovém zobrazení představuje každá buňka samostatnou variantu a v pravém dolním rohu zobrazuje hodnotu zásob na skladě (dostupná fyzická), stejně jako hodnoty **Rezervováno** (fyzická rezervace) a **Objednáno** (seřazeno podle celku) v levém horním rohu. Následující tabulka vysvětluje význam různých hodnot na skladě.

| Hodnota položek na skladě                            | popis |
|------------------------------------------|-------------|
| Číselná hodnota větší než 0 (nula) | Varianta byla uvolněna do vybraného skladového místa a můžete provést další akce v buňce. |
| **0** (nula)                             | Varianta byla uvolněna do vybraného skladového místa, ale položka není k dispozici ve vybraném skladovém místě. Můžete provést další akce v buňce. |
| **není k dispozici** nebo neaktivní buňka              | Varianta nebyla uvolněna do vybraného skladového místa a nemůžete provést další akce v buňce. |

Pořadí zobrazení hodnot dimenze v maticovém zobrazení je založeno na konfiguraci pořadí zobrazení dimenze v centrále Commerce. Konfiguraci pořadí zobrazení dimenze můžete změnit výběrem nové dimenze, kterou chcete použít. 

Následující akce jsou dostupné v buňce maticového zobrazení:

- **Prodat nyní** - Tato akce přidá vybranou variantu do košíku a přesměruje uživatele na obrazovku transakce.
- **Vyzvednout v obchodě** - Tato akce vytvoří objednávku zákazníka pro vybranou variantu, která bude vyzvednuta z vybraného obchodu, a přesměruje uživatele na obrazovku transakce.
- **Expedovat produkt** - Tato akce vytvoří objednávku zákazníka pro vybranou variantu, která bude expedována z vybraného obchodu, a přesměruje uživatele na obrazovku transakce.
- **Dostupnost** - Tato akce uživatele přenese na samostatnou stránku zobrazující množství ATP pro vybranou variantu ve vybraném úložišti.
- **Zobrazit všechna umístění** - Tato akce se přepne do standardního zobrazení seznamu dostupnosti inventáře zobrazujícího informace o zásobách pro vybranou variantu.
- **Zobrazit podrobnosti produktu** - Tato akce přesměruje uživatele na stránku s podrobnostmi o produktu (PDP) vybrané varianty.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Vyhledávací kód přístupu k zásobám z jiných stránek v POS

Uživatelé POS mohou přistupovat k operaci vyhledávání zásob z jiných stránek v POS.

Následující ukázkový obrázek ukazuje výsledky vyhledávacího kódu zásob z PDP v POS.

![Vyhledávání zásob na stránce s podrobnostmi o produktu.](media/inventory-lookup-from-product-details-page.png)

Na PDP hlavního produktu můžete použít akci **Zobrazit všechny varianty** na panelu aplikací pro spuštění matice zobrazení vyhledávacího kódu, které zobrazuje informace o dostupnosti zásob pro aktuální obchod pro všechny varianty produktu. U jednotlivého produktu PDP zobrazuje okamžitou hodnotu množství na skladě (dostupného fyzického) daného produktu pro aktuální obchod. Dále můžete vybrat odkaz **Zásoby jiných obchodů** ke spuštění operace vyhledávání zásob k ověření dostupnosti zásob produktu v jiných obchodech nebo skladech.

> [!NOTE]
> Akce **Zobrazit všechny varianty** v PDP je dostupná jen pro hlavní produkty, které mají varianty. Není k dispozici pro konkrétní produkty nebo sady.

Můžete nakonfigurovat operaci vyhledávání zásob tak, aby se zobrazovala jako odkaz v mřížce tlačítek na obrazovce transakce POS. Po konfiguraci, když uživatel vybere řádek košíku a poté vybere tlačítko **Vyhledávání zásob**, zobrazí se zobrazení seznamu pro vyhledávání zásob pro vybraný produkt. Další informace o tom, jak konfigurovat mřížky tlačítek pomocí nástroje návrháře rozložení obrazovky POS, získáte v tématu [Vizuální konfigurace uživatelského rozhraní POS](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Vyhledávání zásob s výpočtem na straně kanálu

Ve verzi Commerce 10.0.9 a dřívější se hodnota **dostupné fyzické** v operaci vyhledávání zásob načte z centrály Commerce prostřednictvím volání služby v reálném čase. Ve verzi Commerce 10.0.10 a novější můžete nakonfigurovat operaci vyhledávání zásob POS tak, aby k výpočtu dostupné fyzické hodnoty používal výpočet na straně kanálu na serveru Commerce, což může poskytnout spolehlivější a přesnější odhad zásob na skladě započítáním transakčních dat, která ještě nejsou synchronizována s centrálou. Další informace o výpočtu zásob na straně kanálu a související konfiguraci POS v ústředí získáte v části [Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Další prostředky

[Vizuální konfigurace uživatelského rozhraní POS](pos-screen-layouts.md)

[Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
