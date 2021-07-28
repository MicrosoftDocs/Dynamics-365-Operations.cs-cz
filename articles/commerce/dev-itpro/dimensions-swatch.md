---
title: Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky
description: Toto téma popisuje, jak konfigurovat hodnoty dimenze produktu jako vzorníky v centrále Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 513ec2f48a3c7c81a41fd64a9752067d12eb4ec8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353855"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Nakonfigurujte hodnoty dimenze produktu tak, aby se zobrazovaly jako vzorky

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Toto téma popisuje, jak konfigurovat hodnoty dimenze produktu jako vzorníky v centrále Microsoft Dynamics 365 Commerce. Informace o dimenzích produktů získáte v části [Dimenze produktu](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce podporuje použití rozměrů, stylu a barevných rozměrů k reprezentaci variant produktu. Rozměry produktu mají popisné názvy, které se zobrazují na stránkách s podrobnostmi o produktu (PDP), takže lze vybrat varianty produktu. Mezi příklady těchto popisných názvů patří „Malý“, „Střední“ a „Velký“ pro velikosti a „Černý“ a „Hnědý“ pro barvy. Pokud však produkt podporuje mnoho variant, k zobrazení obrázku pro každou variantu produktů je zapotřebí více výběrů. Proto může být pro zákazníky pomalé a zdlouhavé procházet a vybírat varianty produktů.

Když se rozměry na PDP zobrazují jako vzorky, získají zákazníci vizuální náhled na varianty produktu. Mohou snadno procházet širokou škálu barev, vzorů a textur a mohou rychle prohlížet různé kombinace variant produktu.

Funkce zobrazení rozměrů jako vzorků umožňuje Commerce používat hexadecimální (hex) kódy a obrázky k zobrazení rozměrů jako políček. Podobné dimenze, například barvy, lze navíc seskupit na stránkách seznamu produktů. Například zákazník hledá produkty, které jsou modré. Pokud jsou různé hodnoty modré dimenze seskupeny, stránka seznamu výsledků hledání zobrazuje produkty, které mají různé odstíny modré. Seskupení dimenzí významně zlepšuje zkušenosti se zdokonalováním produktů a pomáhá zákazníkům najít více produktů prostřednictvím jediného vyhledávacího dotazu na produkt.

> [!NOTE]
> Funkce rozměrů displeje jako políčka je k dispozici od Dynamics 365 Commerce verze 10.0.20.

Následující ilustrace ukazuje příklad, kdy se barvy objeví jako vzorky na Commerce PDP.

![Příklad barev zobrazených jako vzorky na stránce s podrobnostmi o produktu.](../dev-itpro/media/swatch_pdp.png)

Následující ilustrace ukazuje příklad, kdy se barvy objeví jako vzorky na stránce se seznamem výsledků vyhledávání Commerce.

![Příklad barev zobrazených jako vzorky na stránce se seznamem výsledků hledání.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>V centrále Commerce povolte zobrazení rozměrů jako vzorků

Chcete-li povolit rozměry zobrazení jako vzorky v centrále Commerce, přejděte na **Pracovní prostory \> Správa funkcí** a zapněte funkci **Povolit podporu obrázků pro hodnoty dimenzí produktu**. Když je tento příznak funkce povolen, přidají se tři nová pole pro každou dimenzi do příslušných tabulek v centrále Commerce: **Hexadecimální kód**, **URL** (pro obrázky) a **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Nakonfigurujte hodnoty dimenzí v centrále Commerce

Zobrazení dimenzů jako vzorků je podporováno pro rozměry, styl a barevné rozměry. Hodnoty hexadecimálního kódu a adresy URL obrázku pro příslušné dimenze lze určit v centrále Commerce. Ve výchozím nastavení, pokud pro dimenzi nejsou poskytnuty hodnoty hexadecimálního kódu a adresy URL obrázku, systém zobrazí text popisného názvu dimenze.

Konfiguraci lze provést na kterékoli z následujících úrovní:

- **Dimenze** - V centrále Commerce otevřete stránku dimenze hledáním **Barva**, **Velikost** nebo **Styl**. Na každé stránce jsou v mřížce uvedeny hodnoty dimenzí. Můžete spravovat pořadí zobrazení, hexadecimální kód a hodnoty adresy URL obrázku. Následující ilustrace znázorňuje příklad konfigurace na stránce **Barvy**.

    ![Příklad konfigurace dimenzí na stránce Barvy.](../dev-itpro/media/swatch_Color.PNG)

- **Skupina dimenzí** - V Dynamics 365 Commerce můžete použít vlastnost **RefinerGroup** k vytvoření skupin dimenzí. Pokud jsou definovány skupiny dimenzí, otevřete příslušnou stránku vyhledáním **Skupiny barev**, **Velikostní skupiny** nebo **Skupiny stylů**. Na každé stránce můžete spravovat hexadecimální kód, adresu URL obrázku a hodnoty skupiny rafinování. Následující ilustrace znázorňuje příklad konfigurace na stránce **Skupiny barev**.

    ![Příklad konfigurace dimenzí na stránce Skupiny barev.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Dimenze produktu (během vytváření produktu)** - Když vytváříte nový produkt, můžete použít stránku **Rozměry produktu** pro zadání hodnot dimenzí. U stávajících produktů již mohou být pole **Hexadecimální kód**, **URL** (pro obrázky) a **RefinerGroup** nastavena. Hodnoty v tomto poli však můžete podle potřeby měnit. Následující ilustrace znázorňuje příklad konfigurace na stránce **Dimenze produktů**.

    ![Příklad konfigurace dimenzí na stránce Dimenze produktů.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Proces správy konfigurací hexadecimálního kódu a adresy URL obrázku se řídí stejným vzorem, který se používá ke správě pořadí zobrazení dimenzí.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Nakonfigurujte hodnoty dimenzí pomocí hexadecimálních kódů

U většiny barevných dimenzí by měla být na stránkách dimenzí v obchodním sídle uvedena hodnota barvy hexadecimálního kódu. Například černá barva by měla mít hexadecimální kód **#00000**. Když Commerce vykreslí webovou stránku, hexadecimální kód je reprezentován barevným vzorníkem.

Následující obrázek ukazuje příklad, kde jsou barevné rozměry konfigurovány pomocí hodnot hexadecimálního kódu.

![Příklad konfigurace dimenzí, které využívají hexadecimální kód.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Nakonfigurujte hodnoty dimenzí pomocí adres URL obrázků

Některé barevné rozměry představují vzory, nikoli plné barvy. Například barevnou dimenzi lze popsat jako „leopard“. V těchto případech můžete efektivněji reprezentovat barevné rozměry pomocí publikovaných obrázků místo hexadecimálních kódů pro vzorky.

Každý obrázek musíte nahrát do nástroje pro tvorbu webů Commerce a publikovat ho. Poté zadejte adresu URL obrázku pro publikovaný obrázek na příslušných stránkách dimenzí v obchodním sídle. Pokud byla vybrána dimenze pro zobrazení jako vzorník, ale hexadecimální kód není definován, provede Commerce při vykreslení stránky vyhledávání obrázků. Pokud vyhledávání obrázků selže, zobrazí Commerce text popisného názvu dimenze.

Následující ilustrace znázorňuje příklad, kdy je adresa URL používána pro konfiguraci na stránce **Barvy**.

![Příklad konfigurace dimenzí, které využívají adresy URL obrázků.](../dev-itpro/media/swatch_color_urls.PNG)

K definování adres URL obrázků můžete použít mediální šablonu, stejně jako u obrázků produktů a kategorií. Když nahráváte obrázky do nástroje pro tvorbu webů, konvence názvů souborů a cesty k souborům musí být konzistentní.

Následující ilustrace znázorňuje příklad, kdy je adresa URL používána pro konfiguraci šablony médií.

![Příklad konfigurace šablony média.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Nakonfigurujte hodnoty dimenzí pomocí hexadecimálních kódů a adres URL obrázků

U většiny barevných dimenzí můžete konfigurovat hexadecimální kódy i adresy URL obrázků. Logika záložní vykreslování Commerce automaticky vyhledá hexadecimální kód nebo adresu URL obrázku, aby zobrazila vzorník barev. Použitím hexadecimálních kódů i adres URL obrázků ke konfiguraci rozměrů barev pomůžete zjednodušit správu obrázků, pokud je počet barev velký.

Následující ilustrace znázorňuje příklad, kdy se použije hexadecimální kód i adresa URL pro konfiguraci na stránce **Barvy**.

![Příklad konfigurace dimenzí, které využívají hexadecimální kód i adresy URL obrázků.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Nakonfigurujte skupiny zpřesnění

Když definujete hexadecimální kód nebo adresu URL obrázku pro hodnotu dimenze, můžete také určit hodnotu pro pole **RefinerGroup**. Toto pole definuje dimenzi, která by měla být použita ke seskupení podobných hodnot dimenze v prostředí zpřesnění.

Pokud jsou například hodnoty barevných dimenzí „modrá“, „modrá kostkovaná“, „modrá barva“ a „tmavě modrá“, každá hodnota je namapována na jiný hexadecimální kód nebo adresu URL obrázku. Každá hodnota se proto na PDP a produktových kartách u příslušných produktů zobrazí jako odlišná barva. Pokud však namapujete všechny tyto hodnoty kót barev na hodnotu **RefinerGroup** **Modrý**, hledání „modrých“ produktů vygeneruje výsledky vyhledávání na stránce seznamu pro produkty, které mají hodnoty barevných dimenzí „modrá“, „modrá kostkovaná“, „modrá barva“ a „tmavě modrá“.

Příklad na následujícím obrázku ukazuje vztah mezi vlastnostmi **Barva** a **RefinerGroup** v centrále Commerce.

![Příklad správy skupiny zpřesnění.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Správa obrázků v konfigurátoru webů Commerce

Pokud se pro libovolné hodnoty dimenze používají adresy URL obrázků, je nutné příslušné obrázky nahrát do nástroje pro tvorbu webů Commerce. Umístění každého obrázku by mělo odpovídat názvu souboru a cestě ke složce, které jsou definovány pro obrázek v centrále Commerce. Soubory obrázků musí být nahrány do příslušných umístění kategorií v nástroji pro tvorbu webů. Například barevné obrázky musí být nahrány do složky kategorií **Barva**. Další informace o tom, jak nahrávat obrázky do Tvůrce webů, získáte v tématu [Nahrání obrázků](../dam-upload-images.md).

Následující obrázek ukazuje příklad, kde dialogové okno **Nahrát soubory** se používá k nahrávání obrázků do knihovny médií Tvůrce webů. Zdůrazňuje kategorie **Velikost**, **Barva** a **Styl**, které jsou k dispozici pro výběr.

![Příklad kategorií obrazových souborů během nahrávání do knihovny médií tvůrce webů.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Povolit zobrazení vzorků na stránkách webu elektronického obchodování

Před zobrazením vzorků na stránkách webů elektronického obchodování, které vyžadují výběr dimenzí, jako jsou PDP a stránky se seznamy, musíte nakonfigurovat nastavení webů dimenzí v centrále Commerce. Další informace viz [Použít nastavení webu pro dimenze](../dimension-settings.md).

Kromě toho byste měli povolit **Zahrňte atributy produktu do výsledků vyhledávání** vlastnost pro moduly výsledků hledání. Pokud váš web používá přizpůsobené stránky kategorií, měli byste aktualizovat moduly výsledků vyhledávání, které se na těchto stránkách používají, aby byla povolena vlastnost **Zahrňte atributy produktu do výsledků vyhledávání**. Další informace naleznete v tématu [Modul výsledků vyhledávání](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>Zobrazte vzorky v POS a dalších kanálech

Commerce aktuálně nemá dodávanou implementaci, která podporuje zobrazení vzorků v Point of Sale (POS) a dalších kanálech. Funkci zobrazení vzorníku však můžete implementovat jako rozšíření, díky němuž rozhraní API kanálu vrátí hexadecimální kódy a adresy URL obrázků, které jsou nutné k vykreslení vzorníků.

## <a name="additional-resources"></a>Další prostředky

[Modul výsledků hledání](../search-result-module.md)

[Použít nastavení webu pro dimenze](../dimension-settings.md)

[Dimenze produktu](../../supply-chain/pim/product-dimensions.md)

[Nahrát obrázek](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
