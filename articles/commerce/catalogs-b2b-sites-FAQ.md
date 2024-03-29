---
title: Nejčastější dotazy ke katalogům Commerce
description: Tento článek poskytuje odpovědi na nejčastější dotazy týkající se katalogů Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168978"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Nejčastější dotazy ke katalogům Commerce

[!include [banner](includes/banner.md)]

Tento článek poskytuje odpovědi na nejčastější dotazy týkající se [business-to-business (B2B) katalogů](catalogs-b2b-sites.md) Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Proč nemohu konfigurovat hierarchii navigace specifickou pro katalog nebo zobrazit možnost přidružení hierarchie zákazníka?

Ujistěte se, že je povolena funkce **Povolit použití více katalogů na maloobchodních kanálech** v pracovním postupu **Správa funkcí** Commerce headquarters a že máte prostředí verze Commerce 10.0.27 nebo novější. Ujistěte se, že jste vybrali **B2B** jako **Typ katalogu**.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Mohu zobrazit hierarchii specifickou pro katalog a rozšířit stránky kategorií v nástroji Commerce Site Builder?

Ano, uživatelé nástroje Commerce Site Builder, kteří mají v tomto nástroji přístup ke stránce **Produkty**, mohou vybrat katalog a zobrazit hierarchii specifickou pro katalog. Na stránce **Produkty** mohou uživatelé také rozšířit stránku kategorie o konkrétní kategorii v katalogu. Další informace naleznete v tématu [Rozšíření cílové stránky kategorie](enrich-category-page.md). Pokud chcete mít rozšíření, které je specifické pro katalog, doporučujeme, abyste pro tento katalog měli samostatnou a jedinečnou navigační hierarchii.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Může zákazník B2B nakupovat z více katalogů v jedné transakci?

Ano, nákupy z více katalogů v jedné transakci jsou povoleny. Zákazníci B2B mohou pomocí indikátoru katalogu v zobrazení košíku určit, ze kterých katalogů byly konkrétní položky přidány.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Pokud zákazník B2B koupí stejnou položku z různých katalogů, jaké je očekávané chování?

Přestože daný uživatel může mít v daný čas přístup k více katalogům, očekává se, že produkty v těchto katalozích se budou vzájemně vylučovat. Jinými slovy, v ideálním případě by stejný produkt neměl být součástí více než jednoho katalogu pro daného uživatele.

Pokud však nastane situace, kdy stejný produkt patří do více katalogů, systém bude pro tento produkt udržovat více řádků košíku. Pro každý katalog bude samostatný řádek. Stejný produkt ze dvou různých katalogů nebude při placení sloučen.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Když nakupuje zákazník B2B, existuje nějaké ověření dostupnosti katalogu?

Ano. Zákazník B2B bude moci přejít k pokladně pouze v případě, že všechny položky v košíku jsou z platných katalogů. Pokud jsou některé položky košíku z katalogů s prošlou platností nebo odvolaných katalogů, budou odstraněny a uživatel bude informován.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Je během nakupování vyhledávání a objevování produktů (včetně souvisejících a doporučených kolekcí produktů) specifické pro katalog?

Ano. Jakmile si uživatel vybere konkrétní katalog, celá nákupní cesta se zaměří na tento katalog. Tato cesta zahrnuje zkušenosti s objevováním produktů, jako jsou návrhy vyhledávání, výsledky vyhledávání, výsledky kategorií, upřesnění, ceny, atributy a doporučené produkty (jako jsou nové, nejprodávanější, trendy, často nakupované společně a související produkty).

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Může zákazník B2B nakupovat z výchozího sortimentu (catalogID=0)?

Ne, zákazník B2B nesmí nakupovat z výchozího sortimentu. Tento sortiment je určen pouze pro anonymní prohlížení. Pokud zákazníkovi B2B chybí přiřazení katalogu (čeká na aktualizace z jeho správy), neuvidí žádné katalogy, ze kterých si může vybrat, a nebude viditelná žádná hierarchie kategorií.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Může být marketingový obsah uspořádán pro produkt, který je specifický pro katalog?

V současné době je rozšíření produktu podporováno pouze na úrovni webu a kanálu. Jinými slovy, pokud je produkt rozšířen, je sdílen ve více katalozích a odpovídající stránka s podrobnostmi o produktu (PDP) pro tento produkt bude vykreslena stejným způsobem ve všech katalozích pro daný web. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Je podpora katalogu k dispozici pro online kanály B2B i business-to-consumer (B2C)?

V současné době jsou katalogy Commerce určeny pouze pro B2B online kanály.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Do hierarchie zákazníků byl přidán nový zákazník nebo byla ke katalogu přidružena nová hierarchie, ale katalog není uživateli dostupný. Proč?

Spusťte úlohy **1010** poté, co jste nového zákazníka přiřadili k existující hierarchii zákazníků, a když jste vytvořili novou hierarchii zákazníků. Katalogy spojené s hierarchií zákazníků budou viditelné pouze po dokončení úlohy **1010**. Pokud je katalog také nový, ujistěte se, že jste spustili úlohu **1150** (katalog) vedle úlohy **1010**. Stejně jako u každého nového katalogu počkejte, než se data synchronizují s kanálem a indexem vyhledávání. Pokud má úloha stav „Použito“, znamená to, že se data synchronizují do databáze kanálů, ale synchronizace dat s indexem vyhledávání vyžaduje další čas. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Můžeme nastavit návazný a křížový prodej zboží z určitého katalogu?

V současné době jsou podporovány pouze funkce souvisejících produktů. V kontaktních střediscích jsou však dostupné konfigurace položek pro návazný a křížový prodej.

Následující funkce jsou také podporovány pouze v kontaktních střediscích:

- Zdrojové kódy katalogu
- Používání ID zdrojů ke sledování nákladů a míry odpovědí
- Objednávky specifické pro katalog a skripty položek
- Analýza stránky katalogu
- Požadavky na katalog
- Platební kalendáře
- Bezplatné produkty založené na zdrojových kódech

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Můžeme použít zdrojové kódy katalogu pro B2B objednávky prostřednictvím portálu e-commerce?

Ne Zdrojové kódy katalogu jsou podporovány pouze v kanálech kontaktního střediska.

## <a name="additional-resources"></a>Další prostředky

[Vytváření obchodních katalogů pro B2B weby](catalogs-b2b-sites.md)

[Modul pro výběr katalogu](catalog-picker.md)

[Dopad rozšiřitelnosti u přizpůsobení funkce Katalogy Commerce pro B2B](catalogs-b2b-sites-dev.md)
