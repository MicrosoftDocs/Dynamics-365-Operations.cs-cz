---
title: Plánování organizační hierarchie
description: Před nastavením organizací a organizačních hierarchií se ujistěte, že rozumíte tomu, jak nejlépe namodelovat vaše podnikání.
author: sericks007
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef906c0d60639da763f2a9c1e1adf508b0849b8978dff17cd0e7b3936fc4779e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771865"
---
# <a name="plan-your-organizational-hierarchy"></a>Plánování organizační hierarchie

[!include [banner](../includes/banner.md)]

Před nastavením organizací a organizačních hierarchií se ujistěte, že máte plán, jak bude vaše společnost modelována. Organizační model má podstatný vliv na implementaci a obchodní procesy.

Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří podnik. Nejdůležitější věc při modelování organizace je tedy struktura vaší společnosti. Doporučujeme nejprve definovat organizační struktury na základě zpětné vazby od vedoucích pracovníků a manažerů z funkčních oblastí, například finance a účetnictví, lidské zdroje, provoz, nákup a prodej a marketing.

Při plánování hierarchií je také třeba uvážit vztah mezi organizační hierarchií a finančními dimenzemi. Můžete nastavit více organizačních hierarchií představujících různé pohledy na vaši společnost. Použitím finančních dimenzí můžete vytvořit sestavy založené na těchto pohledech. Ve spolupráci se svým partnerem vytvořte hierarchii, která odpovídá potřebám organizačního i statutárního vykazování.

> [!NOTE]
> Ačkoliv lze finanční dimenze použít k reprezentaci právnických osob bez vytvoření právnických osob, finanční dimenze nejsou určeny řešení provozních ani obchodních potřeb právnických osob. Funkce mezijednotkového účetnictví umožňuje pracovat pouze s účetními položkami vytvořenými jednotlivými transakcemi.

> [!IMPORTANT]
> Neměli byste rozhodnout, jak modelovat organizaci, pouze na základě informací v tomto článku. Tato dokumentace je pouze vodítko. Můžete spolupracovat se svým partnerem pro další pomoc. Váš partner získal zkušenost v různých odvětvích a po celé základě odběratelů.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Rozhodněte se, zda chcete modelovat interní organizace jako právnické osoby nebo provozní jednotky

Je nutné mít alespoň jednu právnickou osobu reprezentující vaše podnikání. Právnická osoba může uzavírat právní smlouvy a jsou po ní vyžadovány finanční výkazy s informacemi o jejím výkonu.

Právnické osoby slouží k transakčnímu podnikání nebo pro konsolidaci. To znamená, že právnická osoba ve Finance and Operations nepředstavuje nutně skutečnou entitu ve vašem podnikání. Společnost, která se účastní transakcí, může například vlastnit dceřiné právnické osoby. V tomto scénáři je právnická osoba vyžadována pro transakce a virtuální právnická osoba je vyžadována pro konsolidaci výsledků a zůstatků dceřiných právnických osob.

Interní organizace ve společnosti, jako jsou například místní pobočky, lze znázornit jako další právnické osoby nebo provozní jednotky hlavní právnické osoby. Provozní jednotka nemusí být zákonem definovaná organizace. Provozní jednotky se používají k řízení ekonomických zdrojů a provozních procesů v podnikání. Například oddělení a nákladová střediska jsou provozní jednotky.

Některé funkce fungují jinak v závislosti na tom, zda je organizace právnická osoba a provozní jednotka. Pečlivě zvažte při svém rozhodování funkci popsanou níže.

### <a name="master-data"></a>Hlavní data

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Některá hlavní data, např. odběratelé, platební podmínky, finanční úřady a objednávání specifické pro pracoviště skladu, musí být nastavena pro každou právnickou osobu. Některá hlavní data, například uživatelé, produkty a většina dat lidských zdrojů, jsou sdílena mezi všemi právnickými osobami.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Hlavní data jsou sdílena mezi provozními jednotkami.

### <a name="module-parameters"></a>Parametry modulu

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Parametry pro moduly, jako jsou parametry pohledávek, parametry závazků a peněžní a bankovní parametry řízení, musí být nastaveny podle právnické osoby. Vzhledem k tomu, že nastavení modulu pro právnické osoby samostatné, jednotlivé dimenze mohou splňovat místní zákonné požadavky a obchodní postupy. Například právnická osoba profesionálních služeb a právnická osoba výroby může mít různé parametry modulu, přestože vykazují stejné nadřazené společnosti.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Parametry modulu jsou sdíleny mezi provozními jednotkami.

### <a name="data-security"></a>Zabezpečení dat

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Většina dat jsou automaticky zabezpečena pomocí ID společnosti. ID společnosti je jedinečný identifikátor pro data, která jsou přidružena k právnické osobě. Společnost může být přiřazena pouze jedné právnické osobě a právnická osoba může být přiřazena pouze jedné společnosti. Uživatelé mohou přistupovat k datům pouze pro společnosti, k nimž mají přístup. Není nutné přizpůsobovat k zabezpečení dat podle ID společnosti.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Data lze zabezpečit podle provozní jednotky vytvořením vlastních zásad zabezpečení dat. Zásady zabezpečení dat slouží k omezení přístupu k datům. Předpokládejme například, že má uživatel oprávnění k vytvoření nákupní objednávky pouze v určité provozní jednotce. Zásady zabezpečení dat lze vytvořit pro zabránění uživateli v přístupu k datům nákupní objednávky z jiných provozních jednotek. Objem transakcí a počet zásad zabezpečení může ovlivnit výkonnost. Při navrhování zásady zabezpečení mějte na paměti výkon.

### <a name="ledgers"></a>Hlavní knihy

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Každá právnická osoba vyžaduje hlavní knihu, která poskytuje účtovou osnovu, zúčtovací měnu, měnu vykazování a fiskální kalendář. Rozvahu lze vytvořit pouze pro právnickou osobu. Hlavní účty, dimenze, účetní struktury, grafy účtů a účetní pravidla lze použít ve více než jedné právnické osobě.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Provozní jednotka nemůže mít vlastní údaje hlavní knihy. Pokud vaše interní organizace nevyžadují jedinečné hlavní knihy, můžete je namodelovat jako provozní jednotky. Údaje hlavní knihy budou nastaveny pro nadřazenou právnickou osobu v hierarchii. Výsledovky lze vytvořit pro provozní jednotky v rámci právnické osoby nebo nadřazenou právnickou osobu.

### <a name="fiscal-calendars"></a>Fiskální kalendáře

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Každá právnická osoba má vlastní fiskální kalendář. Pokud vaše interní organizace používají různé fiskální roky a fiskální kalendáře, musíte je namodelovat jako právnické osoby.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Provozní jednotky musí sdílet fiskální kalendář. Pokud vaše interní organizace mohou používat stejné fiskální roky a fiskální kalendáře, můžete je namodelovat jako provozní jednotky.

### <a name="consolidation"></a>Konsolidace

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Chcete-li připravit finanční výkazy, musíte konsolidovat finančních výsledky pro oblastní pobočky do jediné, konsolidované společnosti.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Konsolidace není vyžadována, protože data jsou již sdílena mezi provozními jednotkami.

### <a name="centralized-payments"></a>Centralizované platby

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Centralizované platby musí být nastaveny tak, aby faktury pro všechny dceřiné právnické osoby mohly být placeny do nebo z jedné nadřazené právnické osoby.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Centralizované platby nejsou vyžadovány, protože všechny faktury jsou zaznamenávány v jedné právnické osobě.

### <a name="intercompany-transactions"></a>Mezipodnikové transakce

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Mezipodnikové prodejní objednávky, nákupní objednávky, platby nebo příjmy lze na sebe navzájem aplikovat. Není nutné používat doklady deníku. Můžete zobrazit mezipodnikové transakce na úrovni dílčí hlavní knihy (Pohledávky, Závazky). Následující příklady ilustrují způsob zpracování mezipodnikových transakcí.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Příklad 1: Ústředí poskytuje služby místním pobočkám a musí účtovat náklady těchto služeb místním pobočkám.

Pokud namodelujete místní kancelář jako právnickou osobu, máte následující možnosti:

- Ústředí vytvoří položku deníku pro naúčtování nákladu místní kanceláři. Splatnost transakcí nelze sledovat.
- Ústředí odešle nákupní objednávku za služby místní kanceláři. Je automaticky vytvořena prodejní objednávka v právnické osobě pro místní kancelář s mezipodnikovými transakcemi dílčí hlavní knihy.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Příklad 2: Centrála opatřuje a platí za službu, která je určena pro místní kancelář.

Pokud namodelujete místní kancelář jako právnickou osobu, máte následující možnosti:

- Faktura a platba jsou v souladu s regulačními požadavky ústředí. Ústředí může vytvořit položku deníku pro naúčtování nákladu místní kanceláři. Splatnost transakcí nelze sledovat.
- Faktura a platba jsou v souladu s regulačními požadavky ústředí. Ústředí může vytvořit mezipodnikovou transakci dílčí hlavní knihy.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Mezipodnikové transakce mezi provozními jednotkami jsou podporovány pouze v dokladech deníku. Provozní jednotka může vydávat ani přijímat nákupní objednávky, prodejní objednávky ani faktury od jiné provozní jednotky ve stejné právnické osobě. Nemůžete zobrazit mezipodnikové transakce na úrovni dílčí hlavní knihy (Pohledávky, Závazky). Následující příklady ilustrují způsob zpracování mezipodnikových transakcí.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Příklad 1: Ústředí poskytuje služby místním pobočkám a musí účtovat náklady těchto služeb místním pobočkám.

Pokud namodelujete místní kancelář jako provozní jednotku, ústředí zadá výdajovou transakci a odkóduje ji do místní kanceláře.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Příklad 2: Centrála opatřuje a platí za službu, která je určena pro místní kancelář.

Pokud namodelujete místní kancelář jako provozní jednotku, faktura a platba jsou v souladu s regulačními požadavky ústředí. Faktury lze kódovat k místní kanceláři. Na výkazu zisků a ztrát použijte vyrovnávací finanční dimenze pro vykazování nákladů pro místní kanceláře.

### <a name="local-tax-requirements"></a>Místní daňové požadavky

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Právnická osoba podléhá daňovým zákonů finančního úřadu v zemi nebo oblasti kde je registrována. Například právnická osoba, která je registrována v Dánsku podléhá dánským daňovým zákonům a předpisům. Právnická osoba může patřit pouze do jedné země/oblasti. Země nebo oblast, kterou jste vybrali pro primární adresu právnické osoby, řídí funkce specifické pro zemi/oblast, které jsou k dispozici pro právnickou osobu. Například pokud je primární adresa právnické osoby v Dánsku, funkce, které souvisejí s dánskými daňovými zákony a předpisy jsou k dispozici. Z toho vyplývá, že pokud jsou vaše organizace v různých zemích či oblastech a vyžadují různé místní daňové možnosti, musíte organizace nastavit jako samostatné právnické osoby.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Provozní jednotky používají kontext země nadřazené právnické osoby. Provozní jednotky ve stejné právnické osobě nemohou mít rozdílné požadavky specifické pro zemi/oblast. Pokud vaše organizace jsou ve stejné zemi/oblasti a využívají stejné daňové možnosti, můžete je nastavit jako provozní jednotky.

### <a name="statutory-reporting-for-a-countryregion"></a>Statutární vykazování pro zemi/oblast

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Pro země nebo oblasti, které jsou podporovány, lze vytvořit většinu povinných sestav. 

> [!NOTE]
> Účtovací vrstva v hlavní knize vám umožňuje vytvořit úpravné položky pro nadřazenou společnost, která používá jiný účetní standard než dceřiná společnost. Například pro společnost, která používá obecně přijímanou účetní praxi ve Velké Británii (UK GAAP), můžete vytvořit položky úprav v účtovací vrstvě. Tyto položky mohou konsolidovány do nadřazené společnosti, která používá obecně přijímané účetní principy (GAAP) ve Spojených státech amerických. Položky úprav neovlivní vykazování UK GAAP.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Statutární zprávy musí být vytvořeny jinou aplikací. Je nutné zajistit, že data zachycená v aplikacích Finance and Operations podporují požadavky jednotlivých provozních jednotek, kde se liší od požadavků ústředí.

### <a name="currency"></a>Měna

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Pokud vaše organizace musí používat různé funkční měny, musíte je namodelovat jako právnické osoby. Funkční měny se nastavují na právnickou osobu. Transakce však můžete zadávat v různých měnách.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Pokud vaše organizace mohou používat jednu funkční měnu, můžete organizace namodelovat jako provozní jednotky. Provozní jednotky musí sdílet funkční měnu. Můžete však zadávat transakce a vytvářet sestavy v různých měnách.

### <a name="year-end-closing"></a>Roční uzávěrka

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Pokud se předpisy a účetní postupy liší mezi zeměmi/oblastmi, kde jsou umístěny vaše organizace, mohou vyžadovat různé postupy roční uzávěrky podle organizace. To znamená, že musíte organizace namodelovat jako právnické osoby. Každá právnická osoba má vlastní postupy roční uzávěrky.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Pokud jsou předpisy a účetní postupy stejné v zemích/oblastech, kde jsou umístěny vaše organizace, můžete použít stejné postupy roční uzávěrky. To znamená, že můžete organizace namodelovat jako provozní jednotky. Všechny provozní jednotky musí používat stejný postup roční uzávěrky.

### <a name="number-sequences"></a>Číselné řady

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Číselné řady pro některé odkazy lze nastavit podle právnické osoby. Některé číselné řady mohou být sdíleny.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Číselné řady pro některé odkazy lze nastavit podle provozní jednotky. Některé číselné řady mohou být sdíleny.

### <a name="products"></a>Produkty

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Definice produktů jsou sdílené a je nutné je uvolnit jednotlivým právnickým osobám předtím, než budou moci být součástí transakcí. Každá právnická osoba má vlastní sadu uvolněných produktů, které mohou být zahrnuty v dokumentech transakce. Pokud vaše interní organizace musí používat různé sady produktů, musíte je namodelovat jako právnické osoby.

> [!NOTE]
> I když jsou definice produktů sdílené, u každé právnické osoby, kde je produkt uvolněn, můžete použít různé prodejní, nákupní a skladové parametry pro položku na každém pracovišti skladu.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Všechny provozní jednotky sdílejí stejnou sadu produktů. Pokud vaše interní organizace mohou sdílet stejnou sadu produktů, můžete je namodelovat jako provozní jednotky.

### <a name="inquiry-and-reporting"></a>Dotazy a vytváření sestav

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Pokud organizace modelována jako právnická osoba

Je nutné ručně změnit společnosti pro zadávání transakcí a provádění dotazů ve více právnických osobách. Z důvodu hranic zabezpečení dat může být konsolidované dotazování a vytváření sestav náročné na prostředky a čas.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Pokud organizace modelována jako provozní jednotka

Chcete-li mít přístup k datům z několika provozních jednotek, nepotřebujete měnit společnosti. Konsolidované dotazování a vytváření sestav a jednotlivé místní dotazování je snazší a rychlejší.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Doporučené postupy pro modelování organizací a hierarchií

Při implementaci organizační hierarchie berte v úvahu následující doporučené postupy:

- Vytvořte oddělení pro modelování průniku mezi právnickou osobu a obchodní jednotkou. Můžete pak také zahrnout data z oddělení do právnické osoby pro statutární vykazování a z oddělení do obchodní jednotky pro interní vytváření sestav. Oddělení mohou sloužit jako střediska zisku. Pokud používáte oddělení, nemusíte používat právnické osoby a obchodních jednotky jako dimenze v účetní struktuře. Jako dimenze můžete používat pouze oddělení. Je však nutné používat nákladová střediska a oddělení jako dimenze v účetní struktuře, pokud nákladová střediska jsou používána pouze jako akumulátory nákladů a oddělení slouží k přiznávání výnosů.
- Namodelujte více hierarchií pro provozní jednotky, pokud máte složité požadavky na vykazování zisků a ztrát.
- U jedné právnické osoby nemodelujte více hierarchií pro stejný účel hierarchie.
- Nevytvářejte hierarchii pro každý účel. Obvykle můžete použít jednu hierarchii pro několik účelů. Například jedna hierarchie provozních jednotek může být přiřazena ke všem účelům souvisejícím se zásadami.
- Vytváření vyrovnaných hierarchií. V hierarchii všechny uzly, které jsou stejně vzdáleny od kořenového uzlu jsou definované jako úroveň. Ve vyrovnané hierarchii se může vyskytnout pouze jeden typ provozních jednotek a vzdálenost od kořenového uzlu ke každé úrovni je konzistentní. Jestliže jsou mezilehlé úrovně mezi oddělením a právnickou osobou nebo obchodní jednotkou, může být nutné vytvořit zástupné organizace pro vytvoření vyrovnané hierarchie.
- Nemodeluje oddělenou hierarchii provozních jednotek, jestliže je struktura pro právnické osoby také vaší provozní strukturou. Smíšená hierarchie právnických osob a provozních jednotek může sloužit oběma účelům.
- Před modelováním významných restrukturalizačních scénářů využijte data platnosti hierarchie k provedení analýzy dopadů a testu ověření.
- V režimu konceptu můžete změnit hierarchii před publikováním nové verze v produkčním prostředí.
- Omezte počet uživatelů, kteří mají oprávnění přidávat nebo odebírat organizace z hierarchie v produkčním prostředí. Menší počet snižuje riziko nákladné chyby a nutných oprav.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
