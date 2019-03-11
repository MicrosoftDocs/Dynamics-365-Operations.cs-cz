---
title: Vyhledávání zásob v pokladním místě (POS)
description: V tomto tématu jsou popsány možnosti, které jsou k dispozici pro zobrazení informací o zásobách v pokladním místě.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "314410"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Vyhledávání zásob v pokladním místě (POS)

[!include [banner](includes/banner.md)]

Vyhledávání zásob v pokladním místě pomáhá maloobchodním prodejcům dosáhnout provozní kvality v reálném čase a získat přehledy připojením obchodů, pokladního místa a účetního systému. Tato funkce poskytuje přesné zobrazení zásob produktu v reálném čase napříč obchody a distribučními centry. Rovněž pomáhá maloobchodním prodejcům využít další efektivní možnosti a úspory nákladů díky zlepšenému plánování zásob v reálném čase.

Přesné zobrazení zásob v reálném čase napříč organizací pomáhá zaměstnacům obchodu poskytovat včasný a vynikající zákaznický servis. Nejdůležitějším okamžikem je okamžik, kdy je zákazník připraven k rozhodnutí o koupi. Je důležité, aby pokladníci v obchodě měli k dispozici informace o zásobách v reálném čase, aby mohli přesně zaručit dodání a vyzvednutí produktu.

Stránku **Vyhledávání zásob** můžete otevřít z pracovních prostorů **Retail Modern POS** nebo **Retail Cloud POS**.

![Dlaždice vyhledávání zásob na domovské stránce pokladního místa](media/POSHomepage.png)

Na stránce **Vyhledávání zásob** můžete použít číselnou klávesnici pro zadání čísla produktu. Poté můžete zobrazit množství na skladě pro více obchodů a skladů.

![Standardní stránka vyhledávání zásob](media/InventoryLookUp.png)

Pro každé skladové místo se rovněž zobrazují **Rezervovaná** a **Objednaná** množství.

- **Rezervované** – Toto množství se vztahuje k hodnotě **Fyzicky rezervováno** z účetního systému pro zadané číslo produktu na daném skladovém místě.
- **Objednané** – Toto množství se vztahuje k hodnotě **Objednáno celkem** z účetního systému pro zadané číslo produktu na daném skladovém místě.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Skladová místa, pro která se zobrazují informace o dostupnosti zásob

Seznam skladových míst obsahuje dva typy entit:

- **Maloobchody** – Seznam zobrazuje obchody, které jsou nakonfigurovány pomocí skupiny lokátoru obchodů pro aktuální obchod v modulu Retail headquarters.
- **Distribuční centra** – Různé typy distribučních center (například sklady) lze konfigurovat v aplikaci Microsoft Dynamics 365 for Retail. Seznam však zobrazuje informace o dostupnosti zásob pouze pro distribuční centra výchozího typu **Standardní**.

    > [!NOTE]
    > Informace o dostupnosti zásob se nezobrazuje pro sklady typu **Tranzit**, **Karanténa** a **Zboží v postupu** pro pokladní místo.

Na stránce **Vyhledávání zásob** je možné zobrazit kromě aktuálního množství na skladě, rezervovaného množství a objednaného množství i množství dostupné pro slíbení pro každý obchod. Vyberte obchod, pro který chcete zobrazit informace o množství dostupném pro slíbení, a pak vyberte **Zobrazit dostupnost obchodu**.

![Množství ATP](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Otevření zobrazení matice založené na dimenzi pro zobrazení všech variant

Na stránce **Podrobnosti produktu** základního produktu nebo na stránce **Vyhledávání zásob** vyberte **Zobrazit všechny varianty** z panelu aplikací dolní části stránky. Zobrazení **Matice založená na dimenzi** pro počáteční spuštění z těchto stránkách zobrazuje informace o dostupnosti zásob pro všechny varianty produktu pro aktuální obchod.

> [!NOTE]
> Tlačítko **Zobrazit všechny varianty** je k dispozici pouze pro základní produkty položky, které mají varianty produktu. Není k dispozici pro samostatné produkty nebo sady.

![Tlačítko Zobrazit všechny varianty na stránce vyhledávání zásob](media/StandardToMatrix.png)

Vyberte **Zobrazit všechny varianty** na stránce **Podrobnosti produktu** základního produktu nebo na stránce **Vyhledávání zásob** bez výběru skladového místa, přejděte na zobrazení **Matice založená na dimenzi** pro zobrazení informací o dostupnosti zásob pro všechny varianty produktu pro aktuální obchod.

![Zobrazení Matice založená na dimenzi pro stránku Vyhledávání zásob](media/Matrix.png)

> [!NOTE]
> Na předchozím obrázku je pořadí zobrazení dimenzí abecední, vzhledem k tomu, že pro vybraný produkt nebylo nakonfigurováno pořadí zobrazení dimenzí.

V zobrazení **Matice založená na dimenzi** zahrnují buňky pro varianty produktu hodnotu zásob na skladě v pravém dolním rohu. Následující tabulka vysvětluje význam různých hodnot.

| Hodnota položek na skladě                            | popis |
|------------------------------------------|-------------|
| Číselná hodnota větší než 0 (nula) | Varianta byla uvolněna do vybraného skladového místa a můžete provést další akce v buňce. (Tyto akce jsou popsány podrobněji dále v tomto tématu.) |
| **0** (nula)                             | Varianta byla uvolněna do vybraného skladového místa, ale položka není k dispozici ve vybraném skladovém místě. Lze však provést další akce v buňce. (Tyto akce jsou popsány podrobněji dále v tomto tématu.) |
| **není k dispozici** nebo neaktivní buňka              | Varianta nebyla uvolněna do vybraného skladového místa a nemůžete provést další akce v buňce. |

Výběrem nové dimenze, kterou chcete použít, můžete také změnit pivot pro dimenze.

![Změna pivotu](media/ChangePivot.png)

![Pivot změněn](media/PivotChanged.png)

> [!NOTE]
> Na předchozím obrázku je vlastní (neabecední) pořadí zobrazení dimenzí pro vybraný produkt. Je založeno na pořadí zobrazení dimenzí nastaveném v účetním systému.

Dále lze provést v zobrazení **Matice založená na dimenzi** další akce pro zlepšení produktivity zaměstnance obchodu. Několik příkladů:

- Změňte umístění obchodu pro vyhledání skladové dostupnosti všech variant produktu na jiných skladových místech. Tato umístění zahrnují jiné obchody ve skupině lokátorů obchodů a distribučních centrech výchozího typu **Standardní**.
- Prodejte jednotlivou variantu produktu odběrateli pomocí velkoobchodního prodeje za hotové, vyzvednutí v obchodě nebo expedice na adresu.
- Poskytněte odběrateli informace o dostupných položkách pro slíbení jednotlivých variant produktu v konkrétním místě.

![Další akce na dlaždicích variant](media/VariantActions.png)

> [!NOTE]
> Na předchozím obrázku je pořadí zobrazení dimenzí abecední, vzhledem k tomu, že pro vybraný produkt nebylo nakonfigurováno pořadí zobrazení dimenzí.

Následující tabulka uvádí více informací o dalších dostupných akcích.

| Akce               | popis |
|----------------------|-------------|
| Prodat nyní             | Přidejte vybranou položka varianty k transakci a přesměrujte uživatele na obrazovku transakce. (Tato akce není k dispozici, když je zvoleným místem distribuční centrum.) |
| Vyzvednout z obchodu     | Vytvořte objednávku odběratele pro variantu produktu, která bude vyzvednuta z vybraného umístění, a přesměrujte uživatele na obrazovku transakce. (Tato akce není k dispozici, když je zvoleným místem distribuční centrum.) |
| Dodat produkt         | Vytvořte objednávku odběratele pro variantu produktu, která bude expedována z vybraného umístění, a přesměrujte uživatele na obrazovku transakce. |
| Dostupnost         | Zobrazte informace o položkách dostupných pro slíbení pro vybranou kombinaci variant pro vybrané umístění. |
| Zobrazit všechna místa   | Přepněte na standardní zobrazení vyhledávání zásob a zvýrazněte informace o dostupnosti zásob pro variantu položky napříč všemi obchody ve skupině lokátorů obchodů a distribučních centrech typu **Standardní/Výchozí**. |
| Zobrazit podrobnosti produktu | Přesměrujte uživatele na stránku **Podrobnosti produktu** přidruženého základního produktu. |
