---
title: "Vytváření modelu konfigurace produktu"
description: "V jak vztahu mezi společnostmi, tak mezi podniky a odběrateli se stalo pravidlem, že konfigurace produktů musí splňovat zvláštní požadavky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 901d5dd18f0da6f05c185c24b3f11fe32fdc400b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="build-a-product-configuration-model"></a>Vytváření modelu konfigurace produktu

[!include[banner](../includes/banner.md)]


V jak vztahu mezi společnostmi, tak mezi podniky a odběrateli se stalo pravidlem, že konfigurace produktů musí splňovat zvláštní požadavky.

Výrobce, který podporuje scénáře konfigurace objednávky má možnost více pečlivě sledovat potřeby odběratelů. Kromě toho uskladnění polotovarů ve formě obecných komponent namísto dokončených produktů můžete výrobce snížit kapitál, který je vázán na sklad.  

Úspěšný přesun z nastavení výroby na sklad pro nastavení konfigurace objednávky vyžaduje pečlivou analýzu struktury produktů, identifikaci skupin výrobků a komponentizace. Ke snížení počtu položek a snížení počtu zboží, které jsou v procesu, je velmi důležité, abyste rozuměli rozhraní produktu a navrhování opětovného použití.  

Existuje několik pravidel modelu konfigurace produktu, jako je modelování založené na roli, založené na dimenzích a založené na omezeních. Studie založené na omezeních metodologie mohou snížit počet řádků kódu v modelech o 50 procent ve srovnání s jinými zásadami modelování. Tato metoda může tedy snížit vlastnictví celkových nákladů (TCO). Přesunutím z modelu založeného na pravidlech, který je založený na kódu X++ do modelu založeného na omezeních, již nevyžadujete vývojářskou licenci za účelem správy modelu výrobku.

## <a name="product-configuration"></a>Konfigurace produktu
Období industrializace vedla k velkému plnění při výrobě vysoce kvalitních výrobků bohatých na funkce za přijatelné ceny. Měřítko hospodářství umožnilo většině uživatelů průmyslového světa nakupovat automobily, televizory, potřeby pro domácnost a jiné zboží, které většina z nás považuje za nezbytnou část našeho každodenního života.  

Když se celá řada výrobků stala komoditami, vzrostla potřeba je odlišit. Okamžitou odpovědí výrobců na tuto výzvu bylo k vytváření variant produktů tak, aby odběratelé měli další možnosti. Tato strategie vedla ke zvýšení výzev o prognózy a také ke zvýšení skladových nákladů a neprodaných produktů, které se staly zastaralé.  

Přijetím filosofie konfigurace pro objednávku mají výrobci možnost uspokojit poptávku odběratelů po jedinečných produktech, zatímco se budou snižovat nebo odstraňovat zastaralé skladové položky. Když je posunuta filozofie výrobu na sklad na filozofii konfigurace pro objednávku, jedna okamžitá výzvu, který přitom vznikne, že musí být vyrovnána potřeba krátké doby realizace proti nízkým zásobám.  

Klíč k úspěchu zde je pečlivě analyzovat nabídku produktů a hledat vzorce jak ve funkcích výrobků a procesech. Cílem je identifikovat obecné součásti, které lze vyrobit stejným vybavením a použít ve všech variantách.  

Nová sada konfigurace funkcí produktu zahrnuje uživatelské rozhraní (UI) zajišťující vizuální přehled o struktuře modelu konfigurace výrobku a také deklarativní syntaxi omezení, která nemusí být kompilována. Z toho vyplývá, že společnosti, které chtějí podporovat konfigurační postup mohou začít mnohem snadněji. Následující části vysvětlují, jak návrhář produktu již nepotřebuje podporu vývojáře k sestavení modelu konfigurace produktu, jejímu otestování a jejímu uvolnění do prodejní organizace.

## <a name="building-a-product-configuration-model"></a>Vytváření modelu konfigurace produktu
Existuje několik postupů, které může uživatel provést k vytvoření modelu konfigurace produktu. Jedna z možností je sledovat postupný tok nejprve vytvořením všech referenčních dat, například základních produktů, jedinečných produktů a provozních prostředků a jejich zahrnutí jako součástí, řádky kusovníku, operace postupu a dalších prvků modelu konfigurace výrobku. Případně můžete vybrat více iterativní přístup vytvořením modelu a následným přidáním referenčních dat, až bude potřeba.

### <a name="components"></a>Součásti

Model konfigurace produktu obsahuje jednu nebo více součástí, které jsou spolu svázány prostřednictvím vztahu dílčích součástí. Součásti jsou definovány jednou a je možné použít vícekrát v jednom nebo nebo více modelech konfigurace produktu. Komponenty jsou hlavní stavební kameny modelu konfigurace produktu a téměř všechny informace o modelu se vztahují k nim.

### <a name="attributes"></a>Atributy

Každá komponenta má jeden nebo více atributů určující její vlastnosti. Vlastnosti jsou uživateli vybírány během procesu konfigurace. Atributy řídí vztahy mezi komponentami a uvnitř komponent prostřednictvím zařazení do omezení nebo výpočtů. Prostřednictvím podmínek, které jsou použity na řádcích kusovníku, lze atributy použít k určení fyzickým částem, které tvoří konfigurovaný produkt. Kromě toho atribut dokáže řídit vlastnosti řádku kusovníku pomocí mechanismu mapování. Podobná funkce existuje pro operace postupu týkající se nastavení zařazení a vlastností.

### <a name="expression-constraints"></a>Omezení výrazu

Použití modelu konfigurace produktu založené na omezeních znamená, že existují určitá omezení, když uživatel vybere hodnoty pro různé atributy. Tato omezení lze implementovat jako omezení výrazu modelu OML. Případně omezení lze provést ve formuláři tabulky omezení.

### <a name="table-constraints"></a>Omezení tabulky

Omezení tabulek mohou být definovaná uživatelem nebo systémem.  

Omezení tabulky uživatelem je vytvořeno uživatelem. Uživatel vybere kombinaci typů atributů k představení sloupců tabulky a poté zadá hodnoty z domén typů vybraných atributů k vytvoření řádků v omezeních tabulky.  

Omezení tabulky definované systémem je definováno výběrem, kterou tabulku produktu Microsoft Dynamics 365 for Operations použít jako odkaz, a poté výběrem polí z této tabulky k seřazení sloupců v omezení. Omezení řádků tabulky jsou řádky tabulky aplikace Dynamics 365 for Operations, které jsou k dispozici v době konfigurace.  

Omezení tabulky je zahrnuto v modelu konfigurace produktu odkazováním na definici omezení tabulky a mapováním odpovídajících atributů v modelu do sloupců v omezení tabulky.

### <a name="calculations"></a>Výpočty

Výpočty představují mechanismus pro provádění aritmetických operací v modelu konfigurace. Výpočet například určuje délku konkrétní části surovin nebo čas zpracování pro operaci leštění. Výpočty jsou nezbytné a nastavení hodnoty pro cílový atribut poté, co se všechny hodnoty atributů, které jsou zahrnuty ve výpočetním výrazu, se staly dostupnými.

### <a name="subcomponents"></a>Dílčí komponenty

Dílčí komponenty představují uzly ve struktuře modelu konfigurace produktu. Pro každý vztah dílčí části musí být specifikován odkaz pro základní produkt, který nastavil technologie konfigurace varianty na konfiguraci založenou na omezení.

### <a name="user-requirements"></a>Požadavky uživatele

Požadavek uživatele obsahuje všechny složky dílčích komponent. Jediný rozdíl spočívá v tom, že požadavek uživatele není vázán na základní produkt. Praktický efekt tohoto rozdílu je, že jakékoli řádky kusovníku nebo operace postupu, které jsou definovány v rámci požadavku uživatele, které jsou sbaleny do struktury nadřazené komponenty kusovníku nebo do postupu. Toto chování se podobá chování fiktivního kusovníku.

### <a name="bom-lines"></a>Řádky kusovníku

Řádky kusovníku jsou k dispozici pro identifikaci výrobního kusovníku pro každou komponentu. Řádek kusovníku musí odkazovat na položku a všechny vlastnosti položky lze nastavit na dlouhodobou hodnotu nebo namapovány na atribut.

### <a name="route-operations"></a>Operace postupu

Operace postupu jsou k dispozici pro identifikaci výrobního postupu. Operace postupu musí odkazovat na definovanou operaci a všechny vlastnosti operace lze nastavit na pevnou hodnotu. Všechny vlastnosti kromě požadavků na zdroje mohou být mapovány na atribut namísto hodnoty.

## <a name="validating-and-testing-a-product-configuration-model"></a>Ověření a testování modelu konfigurace produktu
Ověření modelu konfigurace produktu může probíhat na několika úrovních modelu a může se tedy zabývat různými obory. Nejnižší úroveň je pro jediné omezení výrazu. V takovém případě je obvykle ověřování prováděno návrhářem produktu k ověření správnosti syntaxe výrazu.  

Stejně tak lze samostatně ověřit podmínku pro řádek kusovníku nebo operaci postupu.  

Ověření lze také provést pro definici omezení tabulek definovaných uživatelem. V takovém případě uživatel může ověřit, že hodnoty, které jsou zadány pro každé pole, jsou uvnitř domény odpovídajících typů atributů.  

Nakonec může proběhnout validace pro úplný model konfigurace produktu k ověření správnosti úplné syntaxe, a ověření dodržení všech pojmenování a konvencí modelování.

### <a name="testing"></a>Testování

Testování modelu se podobá spuštění skutečné konfigurační relace. Uživatelé mohou procházet stránky konfigurace a ověřit, zda struktura modelu podporuje proces konfigurace. Uživatel může ověřit správnost hodnot atributů, a že popisy atributů navedou uživatele k vybrání správné hodnoty. Nakonec po dokončení testovací relace se systém pokusí vytvořit kusovník a postup, který odpovídá vybraným hodnotám atributu a který zobrazí chybovou zprávu, pokud dojde k chybě.

### <a name="the-configuration-page"></a>Stránka konfigurace

Pro navigaci mezi komponenty, klepněte na možnost **Další** nebo klikněte na součást ve stromu modelu konfigurace produktu, chcete-li, aby se zaměřovalo na něho.

## <a name="finalizing-a-model-for-configuration"></a>Finalizace modelu pro konfiguraci
Když je modelu konfigurace produktu připraven pro použití v scénářích konfigurace pro objednávku, musí být vytvořena verze. Existuje však několik možností, které mohou zlepšit modelování.

### <a name="user-interface"></a>Uživatelské rozhraní

Konfiguraci uživatelského rozhraní lze upravit zavedením skupin atributů v jedné nebo více dílčích komponentách. Tyto skupiny mohou zvýraznit vztahy mezi konkrétními atributy a pomoci uživatelům konfigurace identifikovat oblast produktu, který je právě aktivní.

### <a name="templates"></a>Šablony

K urychlení procesu konfigurace lze vytvořit jednu nebo více šablon konfigurací. Případně lze vytvořit šablony na podporu konkrétních kombinací atributů, například když se výprodej zaměřuje na určitou sadu funkcí produktu.

### <a name="translations"></a>Překlady

Je-li produkt prodáván v různých zemích či oblastech, lze vytvořit překlady pro všechny texty, které se zobrazí v konfiguraci uživatelského rozhraní. Tento text nezahrnuje pouze název a popis polí, ale také hodnoty textu atributů.

### <a name="versions"></a>Verze

Nejdůležitější a poslední krok při procesu dokončení, je vytvoření nové verze pro modelu konfigurace produktu. Verze představuje vztah mezi základním produktem, který lze vybrat pro konfiguraci na objednávce nebo na řádku nabídky a modelu konfigurace produktu. Před použitím v rámci relace konfigurace musí být schválena a aktivována verze.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Rozšíření modelu konfigurace produktu prostřednictvím rozhraní API
Vyhrazené rozhraní pro programování aplikací (API) bylo implementováno tak, aby partnerům a ostatním, kteří mají vývojářskou licenci, mohly být rozšířeny možnosti modelu konfigurace výrobku. Hlavním cílem bylo stanovit mechanismus, který umožňuje partnerům a zákazníkům, kteří používají existující konfigurátor výrobku, migrovat kód, který je vložen do konfigurátoru výrobku modelů do rozhraní API. Tímto způsobem mohou migrovat jejich modely z konfigurátoru výrobku do konfigurace výrobku. Nový partneři a zákazníci však mohou také využít výhod z rozhraní API k rozšíření nových modelů konfigurace produktu.

### <a name="pcadaptor-class"></a>Třída PCAdaptor

Rozhraní API je implementováno pomocí sady tříd **PCAdaptor**, které zpřístupňují strukturu dat modelů konfigurace produktu. Instanci třídy **PCAdaptor** je nutné vytvořit pro každý model, který bude rozšířen. Po dokončení relace konfigurace systém kontroluje instanci této třídy a spustí ji, pokud ji nalezne.  

Následující vývojový diagram zobrazuje přehled procesu.  

[![Vývojový diagram](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Vývojový diagram rozhraní API konfigurace produktu

## <a name="product-configuration"></a>Konfigurace produktu
Konfigurace produktu lze provést v následujících umístěních:

-   Řádek prodejní objednávky
-   Řádek prodejní nabídky
-   Řádek nákupní objednávky
-   Řádek výrobní zakázky
-   Řádek požadavku na položku (projekt)

Účelem konfigurace je vytvořit varianty jedinečného produktu, který splňuje požadavky odběratele. Pro každou novou konfiguraci je vytvořeno jedinečné ID konfigurace. Toto ID umožňuje sledování skladu.

### <a name="multiple-sites-and-intercompany"></a>Více pracovišť a mezipodniková pracoviště

Bude-li konfigurace provedena na pracovišti nebo dokonce ve společnosti, která se liší od pracoviště nebo společnosti, kde má výroba probíhat, bude pro ně vytvořen kusovník a postup a budou umístěny na webu dodavatele dodavatelské společnosti. Varianty produktu budou vydány do všech společností, které jsou součástí dodavatelského řetězce.




