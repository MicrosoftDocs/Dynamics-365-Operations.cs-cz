---
title: Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje
description: Toto téma popisuje další funkce pro výpočet a použití automatických nákladů pro objednávky kanálů Commerce pomocí funkce rozšířených automatických nákladů.
author: hhaines
manager: annbe
ms.date: 03/30/2020
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
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175124"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a>Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje


[!include [banner](includes/banner.md)]

Toto téma popisuje funkci pro seskupení automatických nákladů na úrovni řádku a jejich poměrné rozdělení na velkoobchodní prodejní řádky. Tato funkce je k dispozici pro transakce vytvořené v pokladním místu (POS) v aplikaci Retail verze 10.0.1 a prodeje, které byly vytvořeny v kontaktním středisku v aplikaci Retail verze 10.0.2.

Tato funkce je k dispozici pouze tehdy, pokud je funkce [rozšířených automatických nákladů](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) zapnuta pomocí možnosti na stránce **Parametry velkoobchodu**. Kromě toho může být rozšířený způsob výpočtu pro automatické náklady použit pouze na maloobchodní prodejní objednávky, které jsou vytvořeny prostřednictvím velkoobchodních kanálů (POS, kontaktní středisko a platforma Dynamics e-Commerce).

Tato nová funkce poskytuje organizacím větší flexibilitu ve způsobu, jakým jsou automatické náklady na úrovni záhlaví vypočítávány a aplikovány na prodejní transakce.

Ve verzích aplikace, které jsou starší než verze 10.0.1, se automatické náklady na úrovni záhlaví, které mají specifický režim relace doručení, počítají pouze v případě, že existuje shoda se způsobem doručení, který je definován na záhlaví prodejní objednávky.

Například automatické náklady na úrovni záhlaví jsou definované pro způsob dodání **99** a způsob dodání **11**. Prodejní objednávka je vytvořena a způsob dodání **99** je definován v záhlaví objednávky. Avšak některé řádky prodeje jsou nastaveny tak, aby byly expedovány pomocí způsobu dodání **11**. V takovém případě se zvažují pouze náklady na úrovni záhlaví propojené se způsobem dodání **99** a použijí se na prodejní objednávku.

V aplikaci Commerce mají náklady na úrovni záhlaví další funkci, která umožňuje definovat [konfiguraci vrstvených nákladů](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) založenu na hodnotě objednávky. Pokud je například hodnota objednávky mezi 50,00 USD a 200 USD, organizace může chtít účtovat poplatek za přepravu ve výši 5 USD. Pokud je však hodnota objednávky mezi 200,01 USD a 500,00 USD, přepravné může být 4,00 USD.

Některé organizace chtějí výhody výpočtu vrstvených nákladů, která je poskytována s náklady na úrovní záhlaví. Ve scénářích, které zahrnují smíšené způsoby dodání, se však také chtějí ujistit, že vypočítané náklady jsou založeny na shodě se způsobem doručení, který je definován na každém řádku prodeje.

Nyní můžete nakonfigurovat automatické náklady na úrovni záhlaví tak, aby byly při výpočtu nákladů zohledněny všechny režimy doručení v objednávce. Tato funkce vyžaduje složitější logiku výpočtu, chcete-li vypočítat náklady na úrovni záhlaví. Logika seskupuje všechny položky, které jsou dodávány pomocí stejného způsobu doručení, a zachází s touto skupinou jako se skupinou výpočtu pro položky, když vypočítává automatické náklady na úrovni záhlaví. Pro položky, které mají stejný způsob dodání, se automatické náklady se počítají na základě kombinované hodnoty prodeje položek. Tímto způsobem je určena odpovídající úroveň automatických nákladů.

Po získání příslušných nákladů na úrovni záhlaví pro řádky prodeje, které jsou dodávány za použití stejného způsobu dodání, jsou vypočtené náklady poměrně rozděleny na úroveň prodejních řádků. Vzhledem k tomu, že tyto náklady jsou na úrovni řádku a nejsou udržovány na úrovni záhlaví, je vytvořeno specifické propojení mezi položkou a hodnotou nákladů, která je pro ně vypočtena. Toto chování může být užitečné při scénářích částečných vrácení, kdy organizace chce refundovat pouze část nákladů namísto celých nákladů, když jsou vráceny pouze některé položky.

## <a name="scenarios"></a>Scénáře

Následující dva ukázkové scénáře ukazují, jakým způsobem jsou tyto náklady vypočteny při použití nové funkce i bez ní.

### <a name="scenario-1"></a>Scénář 1

Tento scénář ukazuje chování, když je možnost **Poměrné rozdělení na odpovídající řádky prodeje** nastavena na **Ne** v nastavení automatických nákladů. (Toto chování odpovídá chování poplatků na úrovni záhlaví ve verzích aplikace, které jsou starší než 10.0.1.)

V tomto scénáři organizace definovala náklady na úrovni záhlaví pro vztah způsobu dodání **99** a vztah způsobu dodání **11**. Nejsou konfigurovány žádné automatické náklady pro způsob dodání **21**.

![Automatické náklady pro způsob dodání 99, když je poměrné rozdělení na odpovídající řádky vypnuto](media/99_disabled.png)

![Automatické náklady pro způsob dodání 11, když je poměrné rozdělení na odpovídající řádky vypnuto](media/11_disabled.png)

V kontaktním středisku je vytvořena prodejní objednávka a způsob dodání je nastaven na **99**. Tato objednávka obsahuje pět položek. Dva řádky objednávky byly konfigurovány pro použití způsobu dodání **99**, dva řádky byly nakonfigurovány pro použití způsobu dodání **11**, a jeden řádek byl nakonfigurován pro použití způsobu dodání **21**, jak je uvedeno v následující tabulce.

| Zboží  | Množství řádků | Způsob doručení | Cena za jednotku |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 USD            |
| 81332 | 1             | 99            | 50 USD            |
| 81333 | 2             | 11            | 30 USD            |
| 81334 | 3             | 99            | 10 USD            |
| 81334 | 3             | 21            | 5 USD             |

V tomto scénáři je celá objednávka vyhodnocena proti tabulce automatických nákladů pro způsob dodání **99**. Celkový součet všech řádků prodeje se používá k určení odpovídající úrovně v konfiguraci automatických nákladů a tyto náklady se použijí na úrovni záhlaví objednávky. V tomto příkladu je celková částka objednávky 165,00 USD a na záhlaví objednávky je použito dopravné 15 USD. Automatické náklady, které jsou nakonfigurovány pro způsob dodání **11** nejsou nikdy odkazovány nebo použity.

V tomto scénáři, pokud zákazník vrátí některé položky na objednávce a pokud [kód nákladů byl nakonfigurován tak, že bude vrácen](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), celkové náklady na úrovni záhlaví se systematicky použijí pro refundaci, i když jsou vráceny pouze některé položky.

### <a name="scenario-2"></a>Scénář 2

V tomto scénáři jsou definovány náklady na úrovni záhlaví pro vztah způsobu dodání **99** a vztah způsobu dodání **11**. Nicméně možnost **Poměrné rozdělení na odpovídající řádky prodeje** je nastavena na **Ano** pro tyto tabulky automatických nákladů.

![Automatické náklady pro způsob dodání 99, když je poměrné rozdělení na odpovídající řádky zapnuto](media/99_enabled.png)

![Automatické náklady pro způsob dodání 11, když je poměrné rozdělení na odpovídající řádky zapnuto](media/11_enabled.png)

Tento scénář používá stejnou prodejní objednávku, která obsahuje pět řádků. Způsob dodání v záhlaví objednávky je nastaven **99**, ale způsob dodání pro každou položku na prodejní objednávce je nakonfigurován způsobem znázorněným v následující tabulce.

| Zboží  | Množství řádků | Způsob doručení | Cena za jednotku |
|-------|---------------|---------------|----------------|
| 81331 | 1             | 11            | 10 USD            |
| 81332 | 1             | 99            | 50 USD            |
| 81333 | 2             | 11            | 30 USD            |
| 81334 | 3             | 99            | 10 USD            |
| 81334 | 3             | 21            | 5 USD             |

Vzhledem k tomu, že konfigurace automatických nákladů je nastavena na poměrné rozdělení na odpovídající řádky prodeje, systém provede následující kroky výpočtu.

1. Všechny položky, které mají stejný způsob dodání, jsou seskupeny a systém vypočítá celkovou hodnotu položek ve skupině.

    **Způsob doručení 11**

    - Položka 81331, množství 1 = 10 USD
    - Položka 81333, množství 2 = čistá částka 60 USD (30 USD za jednotku)
    - **Celková hodnota produktu pro způsob dodání 11 = 70 USD**

    **Způsob doručení 99**

    - Položka 81332, množství 1 = 50 USD
    - Položka 81334, množství 3 = 30 USD čistá částka
    - **Celková hodnota produktu pro způsob dodání 99 = 80 USD**

    **Způsob doručení 21**

    - Položka 81334, množství 3 = 15 USD čistá částka
    - **Celková hodnota produktu pro způsob dodání 21 = 15 USD**

2. Systém vyhledá konfiguraci pro automatické náklady úrovni záhlaví odpovídající zákazníkovi a nastavení způsobu dodání pro každou skupinu položek. Je-li konfigurace nalezena, systém prohledá vrstvenou konfiguraci, aby nalezl náklady, které je třeba uplatnit, na základě celkové hodnoty produktu položek ve skupině způsobu dodání.

    **Způsob doručení 11**

    - Celková hodnota produktu = 70 USD
    - **Hodnota nákladů = 7 USD**

    **Způsob doručení 99**

    - Celková hodnota produktu = 80 USD
    - **Hodnota nákladů = 15 USD**

    **Způsob doručení 21**

    - Celková hodnota produktu = 15 USD
    - **Hodnota nákladů = 0 USD** (Nebyly nakonfigurovány žádné automatické náklady pro tuto kombinaci odběratele a způsobu dodání.)

    ![Náklady způsobu dodání 11 spadají do zvýrazněné úrovně](media/step2mode11.png)

    ![Náklady způsobu dodání 99 spadají do zvýrazněné úrovně](media/step2mode99.png)

3. Systém vypočítá hodnotu nákladů, která by měla být aplikována na každý řádek, na základě logiky poměrného rozdělení, která zohledňuje poměrnou hodnotu řádku ve vztahu k celkové hodnotě produktu skupiny.

    **Způsob doručení 11**

    - Hodnota nákladů = 7 USD
    - Hodnota produktů skupiny = 70 USD
    - Hodnota řádku 1 = 10 USD (= 14,2857 % z hodnoty skupiny)
    - Hodnota řádku 3 = 60 USD (= 85,7143 % z hodnoty skupiny)
    - **Náklady řádku pro řádek 1 = 1 USD**
    - **Náklady řádku pro řádek 3 = 6 USD**

    **Způsob doručení 99**

    - Hodnota nákladů = 15 USD
    - Hodnota produktů skupiny = 80 USD
    - Hodnota řádku 2 = 50 USD (= 62,5 % z hodnoty skupiny)
    - Hodnota řádku 4 = 30 USD (= 37,5 % z hodnoty skupiny)
    - **Náklady řádku pro řádek 2 = 9,38 USD**
    - **Náklady řádku pro řádek 4 = 5,62 USD**

    **Způsob doručení 21**

    - Hodnota nákladů = 0 USD
    - Hodnota produktů skupiny = 15 USD
    - Hodnota řádku 5 = 15 USD (= 100 % z hodnoty skupiny)
    - **Náklady řádku pro řádek 5 = 0 USD**

Proto bude pro tento příklad k položce 81334 přiřazeno přepravné 5,62 USD. Tyto náklady lze zobrazit na stránce **Spravovat náklady** pro řádek prodeje. Následující obrázek znázorňuje, jak vypadá tato stránka pro položku 81334.

![Poměrně rozdělené náklady na řádku prodeje pro položku 81334](media/proratedlinecharge.png)

Pokud je tento způsob výpočtu použit ve scénáři částečného vrácení, je-li kód nákladů vratný, bude vrácena pouze část nákladů, která je tomuto řádku přidělena.

## <a name="additional-resources"></a>Další prostředky

[Omnikanálové rozšířené automatické náklady](omni-auto-charges.md)

[Povolení a konfigurace automatických nákladů podle kanálu](auto-charges-by-channel.md)
