---
title: Správa prodejní ceny v aplikaci Retail
description: Toto téma popisuje koncepty pro vytváření a správu prodejních cen v aplikaci Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3411be3be44b5ca72bcd6b52b335662b1fc16aa4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231169"
---
# <a name="retail-sales-price-management"></a>Správa maloobchodní prodejní ceny

[!include [banner](includes/banner.md)]

Toto téma obsahuje informace o procesu vytváření a správy prodejních cen v Dynamics 365 Commerce. zaměřuje se na koncepty, které jsou zahrnuty v tomto procesu, a na dopady různých možností konfigurace na prodejní ceny.

## <a name="terminology"></a>Terminologie

V tomto tématu se používají následující termíny:

| Termín | Definice, použití a poznámky |
|---|---|
| Cena | Jednoduchá jednotková částka, za kterou se prodává podukt v klientovi pokladního místa nebo na prodejní objednávce. V tomto tématu se termín *cena* vždy vztahuje na prodejní cenu, nikoliv cenu zásob nebo nákladovou cenu. |
| Základní cena | Cena, která se nastavuje v poli **Cena** na uvolněném produktu. |
| Cena na základě obchodních smluv | Cena, která je nastavena na produkt nebo variantu pomocí obchodní smlouvy typu **Cena (prodej)**. |
| Nejlepší cena | Pokud se na produkt může uplatnit více než jedna cena nebo sleva, nejmenší částka ceny a/nebo největší částka slevy, která produkuje nejnižší možnou čistou částku, kterou musí zákazník zaplatit. V tomto tématu se koncept nejlepší ceny vždy vztahuje na „nejlepší cenu“. Tato nejlepší cena se liší od výčtové hodnoty **Nejlepší cena** pro souběžný režim slevy a neměla by se s tímto pojmem zaměňovat. |

## <a name="price-groups"></a>Cenové skupiny

Cenové skupiny jsou centrem správy cen a slev v aplikaci Commerce. Cenové skupiny slouží k přiřazení cen a slev k entitám Commerce (kanálům, katalogům, umístěním a věrnostním programům). Vzhledem k tomu, že se pro všechny ceny a slevy používají cenové skupiny, je velmi důležité, abyste naplánovali, jak je budete používat, než začnete.

Cenová skupina je sama o sobě pouze název, popis, popřípadě priorita cenové kalkulace. Hlavním bodem týkajícím se cenových skupin, který je třeba mít na paměti, je to, že se používají ke správě vztahů N:N, které mají slevy a ceny s entitami Commerce.

Následující obrázek znázorňuje, jak se cenové skupiny používají. Na tomto obrázku si všimněte, že „Cenová skupina“ je doslova centrem správy cen a slev. Enity Commerce, které můžete použít ke správě rozdílových cen a slev, jsou vlevo, a záznamy skutečné ceny a slevy se nacházejí napravo.

![Cenové skupiny](./media/PriceGroups.png "Cenové skupiny")

Při vytvoření cenových skupin nepoužívejte jednu cenovou skupinu pro více typů entit Commerce. V opačném případě může být obtížné určit, proč se konkrétní cena nebo sleva použije na transakci.

Jak ukazuje červená čárkovaná čára na obrázku, Commerce podporuje základní funkcionalitu Microsoft Dynamics 365 cenové skupiny, která je nastavena přímo na odběrateli. V takovém případě však dostanete pouze obchodní smlouvy s prodejní cenou. Pokud chcete použít ceny specifické pro odběratele, doporučujeme, abyste nenastavovali cenové skupiny přímo na odběrateli. Namísto toho bude vhodnější použít umístění. 

Všimněte si, že pokud je skupina cen nastavena u zákazníka, pak se tato cenová skupina spojí se záhlavím prodejní objednávky u objednávek vytvořených pro tohoto zákazníka. Pokud uživatel změní skupinu cen v záhlaví objednávky, bude stará skupina cen nahrazena novou skupinou cen pouze pro aktuální objednávku. Například stará skupina cen nebude mít vliv na aktuální objednávku, ale bude stále spojena se zákazníkem pro budoucí objednávky.

Následující části poskytují více informací o entitách Commerce, které můžete použít pro stanovení odlišných cen při používání cenových skupin. Konfigurace cen a slev pro všechny tyto entity je dvoustupňový proces. Tyto kroky lze provést v libovolném pořadí. Nicméně logické pořadí je nejprve nastavit cenové skupiny na entitách, protože tento krok je pravděpodobně jednorázové nastavení, které se provede během implementace. Poté, když se vytvoří ceny a slevy, můžete nastavit cenové skupiny na těchto cenách a slevách individuálně.

### <a name="channels"></a>Kanály

Pro oblast obchodu je typické mít různé ceny v různých kanálech. Dva hlavní faktory, které ovlivňují ceny specifické pro daný kanál, jsou náklady a místní tržní podmínky.

- **Náklady** – čím dál je kanál od zdroje produktu, tím větší jsou náklady za skladování produktu. Například čerstvé produkty mají omezenou trvanlivost a zvláštní výrobní požadavky (např. vegetační období). Během zimy stojí čerstvý salát pravděpodobně více v severním klimatu než v jižních klimatech. Pokud nastavujete ceny pro kanály napříč velkou zeměpisnou oblastí, pravděpodobně budete chtít nastavit různé ceny v různých kanálech.
- **Místní tržní podmínky** – obchod, který má přímého konkurenta přes ulici, bude mnohem cenově citlivější než obchod, který v blízkosti přímého konkurenta nemá.

### <a name="affiliations"></a>Umístění

Obecná definice umístění je napojení na skupinu nebo přidružení ke skupině. V aplikaci Commerce jsou umístění skupinami odběratelů. Umístění jsou mnohem flexibilnějším nástrojem pro stanovení cen a slev pro zákazníky, než je základní koncept zákaznických skupin a skupin slev v aplikaci Microsoft Dynamics 365. Za prvé, umístění může být použito jak pro ceny, tak pro slevy, zatímco ceny mimo maloobchod mají odlišnou skupinu pro každý typ slevy a ceny. Dále může zákazník patřit k více umístěním, ale může patřit pouze k jedné cenové skupině každého typu mimo maloobchod. Konečně, ačkoli lze umístění nastavit tak, aby byla napojena na zákazníka, nemusí tomu tak být. Lze použít ad-hoc umístění ad pro anonymní odběratele v POS. Typickým příkladem slevy anonymní slevy umístění je sleva pro seniory nebo studenty, kde může odběratel získat slevu pouze tím, že ukáže členskou kartu skupiny.

Ačkoli umístění jsou nejčastěji přidružena ke slevám, můžete je rovněž použít pro nastavení rozdíných cen. Například pokud maloobchodní prodejce prodává zaměstnanci, může chtít změnit prodejní cenu namísto uplatnění slevy na obvyklou cenu. Jako další příklad může prodejce, který prodává spotřebitelům i obchodním zákazníkům, nabídnout obchodním zákazníkům lepší ceny na základě jejich nákupního objemu. Umístění povolují oba tyto scénáře.

### <a name="loyalty-programs"></a>Věrnostní programy

Co se týče cen a slev, věrnostní programy jsou v podstatě pouze umístěním se zvláštním názvem. Ceny i slevy mohou být nastaveny na věrnostní program, stejně jako mohou být stanoveny pro umístění. Způsob, jakým zákazníci získávají věrnostní ceny při transakci nebo objednávce, se však liší od způsobu, jakým získávají ceny umístění. Zákazníci mohou získat věrnostní ceny pouze v případě, že je k transakci přidána věrnostní karta. Když je k transakci přidána věrnostní karta, přidává se také věrnostní program. Věrnostní program pak umožňuje speciální ceny a slevy.

Věrnostní programy mohou mít více úrovní a slevy se mohou lišit pro různé úrovně. Tímto způsobem mohou maloobchodníci dát častým zákazníkům větší odměny, aniž by museli ručně vkládat zákazníky do zvláštní skupiny.

Věrnostní programy mají dodatečné funkce kromě cen a slev. Nicméně z pohledu cen a slev jsou stejné jako umístění.

### <a name="catalogs"></a>Katalogy

Někteří maloobchodníci používají fyzické nebo virtuální katalogy k uvádění výrobků na trh a naceňují je pro zaměřené skupiny zákazníků. Jako součást svého obchodního modelu zaměřeného na marketing prostřednictvím katalogu mohou tito prodejci nastavit rozdílné ceny ve svých různých katalozích. Microsoft Dynamics 365 podporuje tuto funkci tím, že vám umožňuje definovat slevy a ceny specifické pro katalogy, stejně jako můžete definovat slevy specifické pro jednotlivé kanály nebo umístění. Při úpravě katalogu můžete přiřadit cenové skupiny ke katalogu, stejně jako je můžete přidružit k kanálu, umístění nebo věrnostnímu programu.

### <a name="best-practices-for-price-groups"></a>Doporučené postupy pro cenové skupiny

Nepoužívejte cenovou skupinu pro více typů entit. Namísto toho použijte jednu sadu cenových skupin pro kanály, jinou sadu cenových skupin pro umístění nebo věrnostní programy, atd. Můžete použít předponu nebo příponu v názvu cenové skupiny pro vizuální seskupení různých typů cenových skupin, které používáte.

Vyhněte se nastavování cenových skupin přímo na zákazníka. Použijte místo toho umístění. Tímto způsobem můžete přiřadit zákazníkům všechny typy cen a slev, a to nejen obchodní smlouvy s prodejní cenou.+

## <a name="pricing-priority"></a>Priorita cenové kalkulace

Samotnou cenovou prioritou je pouze číslo a popis. Cenové priority lze aplikovat na cenové skupiny, nebo je lze aplikovat přímo na slevy. Při použití cenových priorit umožňují priority prodejci přepsat zásadu nejlepší ceny tím, že řídí pořadí, ve kterém se na produkty použijí ceny a slevy. Větší číslo cenové priority je vyhodnoceno před nižším číslem cenové priority. Navíc pokud se na jakémkoliv čísle priority nalezne cena nebo sleva, ignorují se všechny ceny nebo slevy s nižšími čísly priorit.

Cena a sleva může pocházet ze dvou odlišných cenových priorit, neboť cenové priority se používají nezávisle na cenách a slevách.

Chcete-li použít cenovou prioritu pro ceny, musíte přiřadit cenovou prioritu k cenové skupině a poté vytvořit pro tuto cenovou skupinu obchodní smlouvu s prodejní cenou.

Funkce cenové priority byla zavedena pro podporu scénáře, kdy maloobchodník chce uplatnit vyšší ceny v určité sadě obchodů. Například maloobchodník definoval regionální ceny pro východní pobřeží Spojených států, ale požaduje vyšší ceny některých produktů v obchodech v New Yorku, protože náklady na prodej některých produktů ve městě jsou vyšší anebo protože místní trh snese vyšší cenu.

Jak bylo popsáno v sekci Nejlepší cena v tomto tématu, cenový modul obvykle vybírá nižší ze dvou cen. Proto je maloobchodníkovi obvykle zabráněno, aby použil vyšší cenu ze dvou cen v obchodě, který má cenové skupiny na východním pobřeží i v New Yorku. Pro vyřešení tohoto problému předtím, než byla zavedena funkce s prioritní cenou, musel maloobchodník dvakrát definovat ceny pro každý produkt a nepřiřadit obě cenové skupiny. Případně prodejce musel vytvořit další cenové skupiny, aby izoloval produkty s vyšší cenou od produktů, které mají obvyklé nižší ceny.

Nicméně funkce priority cen umožňuje maloobchodnímu prodejci vytvořit cenovou prioritu pro ceny obchodu, která je vyšší než cenová priorita regionálních cen. Maloobchodní prodejce může případně vytvořit priority cen pouze pro ceny obchodu a ponechat regionální ceny na výchozí prioritě cen, což je 0 (nula). Obě nastavení pomáhají zaručit, že ceny obchodu budou vždy používány před regionálními cenami.

### <a name="pricing-priority-example"></a>Příklad cenové priority

Podívejme se na příklad, kdy ceny obchodu přepisují ostatní ceny.

Národní maloobchodník nastavuje nejvíce cen podle regionu a má čtyři regiony: severovýchod, jihovýchod, středozápad a západ. Určil několik trhů s vysokými náklady, které mohou podporovat vyšší ceny. Tyto trhy jsou v New Yorku, Chicagu a oblasti San Francisco Bay.

V tomto příkladu přejdeme na podrobnosti severovýchodní oblasti. Obchod 1 je v Bostonu a obchod dva se nalézá na Manhattanu. Pro obchod v Bostonu jsou na kanál napojeny dvě cenové skupiny: severovýchod a obchod 1. Pro obchod na Manhattanu jsou na kanál napojeny tři cenové skupiny: severovýchod, NYC a obchod 2.

Prodejce nastaví dvě cenové priority: vysoké náklady mají prioritu 5 a ceny obchodů mají prioritu 10. (Nezapomeňte, že ve výchozím nastavení je cenová priorita \[nula\], a cena nebo sleva, která má vyšší prioritu, se použije před cenou nebo slevou, která má nižší prioritu.) Pro severovýchodní cenovou skupinu je cenová priorita ponechána na výchozí hodnotě **0** (nula). Pro cenovou skupinu NYC je cenová priorita nastavena na **5**, protože New York City je trh s vysokými náklady. U cenových skupin obchod 1 a obchod 2 je cenová priorita nastavena na **10**.

Dva výrobky, které prodejce prodává, jsou výrobek 1, komodita tričko, a produkt 2, módní značkové džíny

| Produkt | Cena pro severovýchodní oblast | Cena v NYC | Cena v obchodě |
|---|---|---|---|
| Tričko | 15 USD | Nenastaveno | Nenastaveno |
| Módní džíny | 50 USD | 70 USD | Nenastaveno |

Tričko se prodává za stejnou cenu (tedy 15 dolarů) v obchodech v Bostonu a Manhattanu, protože je stanovena pouze jedna cena v cenové skupině severovýchodu, která je napojena na oba kanály. Módní džíny se prodávají za 50 dolarů v obchodě v Bostonu, protože tato cena je jedinou cenou, která je k dispozici v tomto obchodě. V obchodě na Manhattanu jsou však k dispozici dvě ceny: 50 a 70 USD. Vzhledem k tomu, že cenová priorita 5 pro cenovou skupinu NYC je vyšší než cenová priorita 0 (nula) pro cenovou skupinu severovýchodu, bude cena v systému POS započítána jako 70 USD.

> [!NOTE]
> Pro každou cenovou prioritu je zapotřebí úplné procházení logikou pro maloobchodní cenový modul. Proto abyste pomohli zachovat výkon výpočtu ceny a slevy, měli byste cenové priority používat střídmě.

## <a name="types-of-prices"></a>Typy cen

V aplikaci Microsoft Dynamics 365 můžete nastavit cenu produktu na třech místech:

- Přímo na produktu (základní cena)
- V obchodní smlouvě s prodejní cenou
- V úpravě ceny

Základní cena a cena obchodní smlouvy jsou součástí základní aplikace Dynamics 365 a jsou k dispozici i v případě, že nepoužíváte aplikaci Commerce. Funkce úpravy cen je k dispozici pouze v aplikaci Commerce. Další část obsahuje více informací o každé z těchto možností nastavení cen a vysvětluje, jak možnosti spolupracují.

## <a name="setting-prices"></a>Nastavení cen

### <a name="base-price"></a>Základní cena

Nejjednodušší místo pro nastavení ceny produktu je přímo na výrobku. Hodnota, kterou nastavíte přímo na výrobku, se často označuje jako základní cena výrobku. Základní cenu nastavíte v poli **Cena** na kartě **Prodej** stránky **Podrobnosti o uvolněném produktu**. Zadaná hodnota je v měně společnosti. Ve výchozím nastavení je cena pro množství 1 měrné jednotky nastavené v poli **Jednotka** na kartě **Prodej**. Skutečná cena za jednotku výrobku je založena na měrné jednotce, množství ceny a měně.

Pokud má výrobek pro každého jednu cenu, základní cena nabízí nejúčinnější způsob, jak spravovat cenu tohoto výrobku. Dokonce i když používáte obchodní smlouvy k nastavení cen, můžete také nastavit základní cenu na výrobku. Pokud pak nepoužijete obchodní smlouvu **Vše**, máte záložní cenu, která se používá, když se neaplikuje žádná obchodní smlouva.

Pokud se měna kanálu liší od měny společnosti, základní cena v tomto velkoobchodním kanálu se určuje použitím převodu měny na cenu, která je nastavena na výrobku.

Přestože cenová jednotka není běžným velkoobchodním scénářem, velkoobchodní cenový modul ji podporuje. Je-li cenová jednotka nastavena na hodnotu jinou než **0** (nula), cena za jednotku se rovná výpočtu Cena ÷ Cenová jednotka. Například pokud je cena produktu 10,00 USD a cenová jednotka je 50, cena za množství 1 je 0,20 USD (= 10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Obchodní smlouva s prodejní cenou

Pomocí deníku obchodních dohod můžete pro každý produkt vytvářet obchodní smlouvy s prodejními cenami. V aplikaci Microsoft Dynamics 365 existují tři rozsahy odběratele pro obchodní smlouvy s prodejní cenou: **Tabulka**, **Skupina** a **Vše**. Rozsah odběratele určuje odběratele, na které se vztahuje daná obchodní smlouva s prodejní cenou.

Obchodní smlouva s prodejní cenou **Tabulka** je pro jednoho odběratele, který je zadán přímo v obchodní smlouvě. Tento scénář není typickým scénářem vztahů mezi obchodními společnostmi a koncovými zákazníky (B2C). Pokud k němu však dojde, velkoobchodní cenový modul použije při určování ceny **Tabulku** obchodní smlouvy.

Obchodní smlouva s prodejní cenou **Skupina** je typ, který se nejčastěji používá. Mimo Commerce jsou obchodní smlouvy prodejní cenou **Skupina** pro jednoduchou skupinu odběratelů. V aplikaci Commerce byl však koncept skupiny odběratelů rozšířen tak, aby byl obecnější cenovou skupinou. Cenovou skupinu lze napojit na kanál, umístění, věrnostní program nebo katalog. Podrobné informace o cenových skupin naleznete v části "Cenových skupin" dříve v tomto tématu.

> [!NOTE]
> Cena obchodní smlouvy se vždy použije před základní cenou.

### <a name="price-adjustment"></a>Úprava ceny

Jako název naznačuje, úprava ceny slouží k úpravám ceny, která byla buď nastavena přímo na produktu nebo nastavena s použitím obchodní smlouvy. Úpravu ceny lze použít pouze ke snížení ceny, nikoliv k jejímu zvýšení. Úprava ceny je doporučeným způsobem pro maloobchodní prodejce k vytvoření, sledování a správě cenových srážek pro jejich produkty v průběhu času.

Existují tři typy úprav cen: snížení o procento, snížení o částku a cena. Na prodejní transakci se vždy uplatňuje úprava ceny typu snížení o procento nebo snížení o částku. Úprava ceny typu ceny se však uplatní pouze v případě, že upravená cena je nižší než cena, která byla stanovena pomocí základní ceny nebo obchodní smlouvy s cenou. Pokud je tedy cena, která je stanovena v úpravě ceny, vyšší než neupravená cena, není úprava ceny použita.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Určení ceny produktu v transakci

Výpočet ceny a slevy na transakci využívá principu nalezení nejlepší ceny pro zákazníka. Podle této zásady platí, že pokud je nalezena více než jedna cena, použije se nejnižší cena Dále je použita kombinace slev, která produkuje největší částku slevy za celou transakci. V některých případech musí být na jediný produkt použita menší sleva, takže další slevy lze uplatnit i na jiné produkty v transakci.

Jediná výjimka ze zásady nalezení nejlepší ceny pro zákazníka je možnost kombinace a shody nejméně nákladných slev. Tato možnost umožňuje nejméně nákladné slevy, které upřednostňuje prodejce při výběru a seskupování produktů. Proto pokud transakce obsahuje více produktů, než je požadováno pro nárok na nejméně nákladnou slevu, cenový modul vybírá výrobky, které produkují pro zákazníka nejmenší možnou částku slevy.

Cenový modul vrátí tři ceny pro každý produkt: základní cenu, cenu obchodní smlouvy a aktivní cenu.

Základní cena je pouze vlastnost produktu a je stejná pro všechny všude.

Pokud je na obchodní smlouvě s prodejní cenou možnost **Najít další** nastavena na **Ano**, použije se jako cena obchodní smlouvy nejnižší cena nalezená pro použitelné obchodní smlouvy s prodejní cenou. Obchodní smlouvy lze nalézt pomocí cenových skupin nebo kódu účtu **VŠE**. Obchodní smlouvy lze také přiřadit přímo k odběrateli. Pokud je možnost **Najít další** nastavena na **Ne**, použije se první cena obchodní smlouvy, která je nalezena. Pokud nebyly nalezeny žádné obchodní smlouvy s prodejní cenou, nastaví se cena obchodní smlouvy na stejnou hodnotu jako je základní cena.

Aktivní cena se vypočítá tak, že se vezme cena obchodní dohody a uplatní se největší cenová úprava, která se vztahuje na výrobek. Pokud nebudou nalezeny úpravy cen, nebo pokud vypočítaná aktivní cena je vyšší než cena obchodní smlouvy, je aktivní cena nastavena na shodnou s cenou obchodní smlouvy. Mějte na paměti, že cenu produktu nelze zvýšit pomocí úpravy ceny. Použitelné úpravy cen lze nalézt pouze pomocí cenových skupin, které jsou přiřazeny ke kanálu, katalogu, umístění nebo věrnostnímu programu.

## <a name="category-price-rules"></a>Cenová pravidla kategorie

Funkce pravidel cen kategorií v aplikaci Commerce vám poskytuje snadný způsob vytvoření nové obchodní smlouvy pro všechny produkty v kategorii. Tato funkce také umožňuje automaticky najít stávající obchodní smlouvy pro produkty v kategorii a nastavit jejich platnost.

Když vyberete možnost vypršení platnosti stávajících obchodních smluv, systém vytvoří nový deník obchodních smluv pro produkty v kategorii, které mají aktivní obchodní smlouvu. Deník je však třeba ručně zaúčtovat. Kromě toho pravidla cen kategorie mohou nalézt stávající obchodní smlouvy pouze v případě, že používáte stejná cenová pravidla cena (pokud vytvoříte nové cenové pravidlo, které používá stejnou předchozí kategorii). Pokud nepoužíváte stejné pravidlo ceny, stávajícím obchodním smlouvám nevyprší platnost.

Ceny mohou být zvýšeny nebo sníženy pomocí polí **Pravidlo ceny** a **Základ ceny** pravidel cen kategorie.

- V poli **Pravidlo ceny** vyberte typ změny ceny, který chcete použít:

    - **Přirážka** – Procento základní ceny se používá k výpočtu prodejní ceny. Například produkt, jehož cena je 10,00 a prodává se za cenu 15,00, má přirážku 50 procent.
    - **Marže** – Procento prodejní ceny se používá k výpočtu výše zisku. Například produkt, jehož cena je 10,00 a prodává se za cenu 15,00, má marži 33,3 procent.
    - **Pevná čáska** – Částka připočítaná k základu ceny se používá k výpočtu prodejní ceny. Například produkt, jehož cena je 10,00 a prodává se za cenu 15,00, má pevnou částku 5,00.

- V poli **Základ ceny** vyberte typ ceny, kterou chcete upravit:

    - **Základní náklady** – Částka, kterou maloobchodní prodejce zaplatil dodavateli.
    - **Základní cena** – Prodejní cena před použitím obchodních smluv a úprav ceny.
    - **Aktuální cena** – Prodejní cena po použití obchodních smluv a úprav ceny.

Pro snadnou aktualizaci cen různých produktů z různých kategorií produktů můžete použít doplňkové kategorie produktů spolu s pravidly cen kategorií.

## <a name="best-practices"></a>Doporučené postupy

Microsoft SQL Server se často používá pro databáze kanálů z důvodu nákladů (zdarma). Mějte na paměti, že SQL Server Express má omezení hardwaru a limity velikosti dat. Pokud neplánujete správně, můžete rychle odosáhnout limitů velikosti dat SQL Server Express. Tento předpoklad platí nejen pro ceny, ale i pro jiné oblasti produktu. Zde je několik doporučených postupů, které mohou pomoci snížit velikost vašich dat:

- Pokud používáte obchodní smlouvy a vaše ceny se mění, měli byste nechat staré obchodní smlouvy vypršet nastavením koncového data. V průběhu času tento přístup pomáhá snížit počet obchodních smluv, které jsou uloženy v databázi kanálů. Pomáhá také snížit množství dat, s nimiž algoritmus výpočtu cen musí pracovat.
- Pokud se vaše ceny liší podle varianty produktu, zvažte použití základní ceny produktu jako ceny nejběžnější varianty. Poté použijte obchodní smlouvy pouze pro ceny variant, které jsou výjimkami. Tento postup umožňuje snížit počet záznamů obchodních smluv. Protože je snadné importovat data do aplikace Microsoft Dynamics 365, můžete být v pokušení importovat obchodní smlouvu pro každou variantu každého produktu. Tento přístup však může vytvořit mnoho obchodních smluv se stejnou hodnotou. To může zbytečně zvýšit velikost vašich dat.
- Aplikace Commerce zpracovává ceny specifické pro jednotlivé varianty v pořadí od nejkonkrétnějšího k nejméně konkrétním. Pokud dimenze produktu nemá vliv na cenu, nemusíte pro ni definovat obchodní smlouvy. Například produkt je k dispozici ve třech barvách a čtyřech velikostech, ale cena se mění pouze podle velikosti. Pokud definujete obchodní smlouvu pro každou variantu, vytváříte 12 záznamů. Místo toho můžete definovat obchodní smlouvu pouze pro každou velikost a ponechat dimenzi barvy prázdnou. V tomto případě vytváříte pouze čtyři záznamy.

    Případně pokud ne každá hodnota dimenze vytváří různou cenu, můžete definovat jednu obchodní smlouvy pro základní produkt a ponechat všechny dimenze produktu prázdné. Pak definujte oddělenou obchodní smlouvu pro každou hodnotu dimenze, která vytváří odlišnou cenu. Například pokud má velikost XXL vyšší cenu, ale všechny další velikosti mají stejnou cenu, potřebujete pouze dvě obchodní smlouvy: jednu pro základní produkt a jednu pro velikost XXL.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Ceny, které zahrnují daň, a ceny bez daně

Při nastavení prodejních cen v aplikaci Dynamics 365 nezadáváte, zda hodnota ceny, kterou nastavujete, zahrnuje daň či nikoliv. Hodnotou je pouze cena. Nicméně nastavení **Cena včetně DPH** na kanálech vám umožňuje nakonfigurovat kanály tak, aby buď zahrnovaly nebo nezahrnovaly daň z ceny. Toto nastavení se nastavuje na kanálu a může se změnit i v jedné společnosti.

Pokud pracujete s oběma typy zahrnuté a nezahrnuté daně, je velmi důležité správné nastavení ceny, vzhledem k tomu, že celková částka, kterou zákazník platí, se změní, pokud se změní nastavení **Cena včetně DPH** na kanálu.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Rozdíly mezi maloobchodní cenou a cenou mimo maloobchod

Jediný cenový modul se používá k výpočtu cen ve všech kanálech: kontaktní středisko, maloobchod a online obchody. To umožňuje jednotné scénáře obchodování.

Cenová kalkulace je určena k práci s maloobchodními entitami namísto entit mimo maloobchod. Konkrétně je modul navržen pro nastavení cen podle obchodu, nikoli skladu.

Cenový modul **nepodporuje** následující cenové funkce:

- Nastavení cen podle dimenzí úložiště lokality nebo lokality a skladu není podporováno. Pokud zadáte dimenzi lokality pouze v obchodních smlouvách, bude cenový modul ignorovat lokalitu a budou používat obchodní smlouvu pro všechny lokality. Pokud určíte jak lokalitu, tak sklad, chování není definováno/testováno, protože se očekává, že maloobchodníci používají cenové skupiny obchodu k řízení cen pro každý obchod/sklad.
- Ocenění založené na atributech není podporováno.
- Předávání slev dodavatelů není podporováno.
- Standardní cenový modul Supply Chain Management podporuje výpočet ceny na základě požadovaného data expedice a požadovaného data příjmu spolu s aktuálním datem. Maloobchodní ceny však v současné době tyto hodnoty nepodporují. Důvodem je to, že u scénářů B2C zákazníci neočekávají, že požadované datum dodání ovlivní cenu položky. V některých případech mají maloobchodníci provoz B2B i B2C. U operací B2B je běžné měnit ceny na základě dodacích termínů. Tito maloobchodníci mohou pro svou firmu B2B použít ceny Supply Chain Management a maloobchodní cenu pro svou firmu B2C. Maloobchodní ceny se na začátku použití, pouze pokud je uživatel aplikace přidán jako uživatel call centra, takže maloobchodníci mohou přiřadit určité uživatele, kteří budou pracovat s cenou Supply Chain Management, a přiřadit několik uživatelů, kteří budou pracovat s maloobchodními cenami, tj. by tito uživatelé měli být přidáni jako uživatelé call centra. Dále platí, že musí být zapnutá vlastnost **Použít k výpočtu cen dnešní datum** v části **Parametry obchodu > ceny a slevy > Různé**. Tímto způsobem mohou udržovat použitou hodnotu parametru účtů pohledávek pro Požadované datum dodání nebo Požadované datum přijetí pro stanovení ceny Supply Chain Management, ale maloobchodní ceny budou pro výpočet ceny nadále používat dnešní datum.

**Pouze** cenový modul podporuje následující cenové funkce:

- Cena je založena na dimenzích produktu, v pořadí od nejkonkrétnější ceny varianty přes nejméně konkrétní cenu varianty, po cenu základního produktu. Cena, která je nastavena pomocí dvou dimenzí produktu (například barva a velikost), se používá před cenou, která je nastavena pomocí pouze jedné dimenze produktu (například velikost).
- Stejnou cenovou skupinu lze použít ke kontrole cen a slev.

## <a name="pricing-api-enhancements"></a>Vylepšení rozhraní API pro ceny

Cena je jedním z nejdůležitějších faktorů, které kontrolují nákupní rozhodnutí mnoha odběratelů, a mnoho zákazníků porovnává ceny na různých webech, než něco nakoupí. Aby se zajistilo, že budou poskytovat konkurenční ceny, maloobchodníci pozorně sledují své konkurenty a často pořádají promoakce. Chcete-li tedy pomoci těmto prodejcům přilákat zákazníky, je velmi důležité, aby vyhledávání produktů, funkce procházení, seznamy a stránka podrobností o produktu zobrazovalo nejpřesnější ceny.

V nadcházejícím vydání aplikace Commerce bude rozhraní API **GetActivePrices** vracet ceny, které zahrnují jednoduché slevy (například jednořádkové slevy, které nezávisejí na jiných položkách nákupního košíku). Tímto způsobem jsou zobrazené ceny blízké skutečné částce, kterou odběratelé za položky zaplatí. Toto rozhraní API bude zahrnovat všechny typy jednoduchých slev: založené na místu, věrnostní, katalogové a založené na kanálu. Rozhraní API navíc vrátí názvy a informace o platnosti pro použité slevy, takže maloobchodní prodejci mohou poskytnout podrobnější popis ceny a vytvořit pocit naléhavosti, pokud platnost slevy brzy vyprší.


[!INCLUDE[footer-include](../includes/footer-banner.md)]