---
title: Katalogy kontaktního střediska
description: Toto téma popisuje funkce kontaktního střediska pro katalogy v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3758ff51de8217a209b40d7dd461e42ea9632f0a
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936875"
---
# <a name="call-center-catalogs"></a>Katalogy kontaktního střediska

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce kontaktního střediska propojené s možnostmi katalogu v aplikaci Dynamics 365 Commerce.

Funkce katalogu v Commerce lze použít pro několik účelů. Funkce katalogu původně byly vytvořeny k podpoře integrace elektronického obchodování třetí strany. Nastavení katalogu společnostem umožňovalo vytvořit skupinu atributů, které mohly být publikovány externě pro spotřebu řešení elektronického obchodování třetí strany.

Po přidání podpory call centra byl koncept katalogu rozšířen tak, aby obsahoval další možnosti podpory a správy funkcí souvisejících s tradičními katalogy marketingu pro spotřebitele. Společnost směřovaná na zákazníka bude často vytvářet tištěné katalogy, které jsou pak odeslány do jednoho či více segmentů odběratelů. Tyto katalogy budou obvykle mít konkrétní promoakce nebo slevy, které budou použity jen v případě, že odběratel poskytne identifikační kód katalogu v době vytvoření objednávky.

Marketingový společnosti zaměřené na odběratele jsou velmi zaměřené na sledování reakcí na tyto katalogy pro zajištění, aby náklady na jejich výrobu a zasílání byly odůvodněné. Aby bylo možné sledovat reakci, je na zadní straně katalogu obvykle vytištěn kód, který je následně požadován a aplikován, když jeho příjemce zavolá a zažádá o zadání objednávky telefonicky (nebo nyní ještě tradičněji může být kód zadán v případě, kdy odběratel vystaví objednávku online). Tam, kde platí různé podmínky odvětví, které slouží k identifikaci kódu sledování tohoto katalogu (včetně klíčového kódu, kódu promoakce, kódu katalogu, zdrojového kódu), odkazujeme na kód v aplikaci Commerce jako na **ID zdrojového kódu**.

## <a name="basic-catalog-setup"></a>Základní nastavení katalogu

Katalog nakonfigurujte použitím položek **Retail and Commerce** \> **Katalogy a sortiment** \> **Všechny katalogy**.

Když vytvoříte nový katalog, je nutné nejprve propojit katalog s jedním nebo více kanály. K tomu se používá pevná záložka **Kanály Commerce** ve formuláři **Nastavení katalogu**. Klikněte na tlačítko **přidat** a vyberte jeden nebo více kanálů. Při vytváření katalogu lze použít pouze položky připojené k vybranému kanálu [sortiment](/dynamics365/unified-operations/retail/assortments).

Pokud chcete přidat produkty do katalogu, musí být vybrána hierarchie navigace. Hierarchie navigace podporuje strukturu kategorie pro katalog. Je třeba vybrat jednu z hierarchie navigace spojenou s maloobchodními kanály vybranými na pevné záložce **Kanály Commerce** stránky **Katalog**. Pokud navigační kanál nebyl spojen s kanálem dříve, přejděte na **Retail and Commerce** \> **Nastavení kanálu** \> **Kategorie a atributy produktů kanálu** pro účely propojení výchozí hodnoty hierarchie navigace s každým z maloobchodních kanálů.

Na kartě nabídky **katalogy** na stránce **nastavení katalogu** klepněte na **přidat produkty** ke konfiguraci produktů k přidání do katalogu, nebo vyberte uzel v hierarchii navigace (výběr uzlu změní prezentaci na obrazovce zobrazení a umožní přidávat produkty do kategorie v katalogu přímo).

Klepnutím na horní uzel hierarchie katalogu se vrátíte zpět k zobrazení záhlaví hlavního katalogu. Podle potřeby nakonfigurujte datum platnosti a datum vypršení podle potřeby na pevné záložce **hlavní**.

Katalog musí být publikován předtím, než bude k dispozici pro používání. Klepněte na tlačítko **ověřit katalog** v nabídce **katalogy** ke zpracování ověření. To je požadovaná akce a ověří, zda je požadované nastavení přesné. Chcete-li zobrazit detaily ověření, klikněte na **Zobrazit výsledky**. Pokud budou nalezeny chyby, musíte opravit data a znovu spustit ověření, dokud nebude úspěšné.

Po potvrzení ověření klepněte na tlačítko **Workflow** v nabídce ke spuštění workflow schválení. Klepněte na tlačítko **odeslat** v nabídce **workflow** ke spuštění procesu. Nakonfigurujte kroky a oprávněné uživatele workflowu z karty **Retail and Commerce** \> **Nastavení centrály** \> **Workflowy Commerce**. Workflow definuje postup potřebný k přesunutí katalogu do stavu **schváleno**. Když je katalog ve stavu **schváleno**, můžete klepnout na možnost **publikovat** v nabídce **katalogy** a proces dokončit. Jakmile je katalog ve stavu **publikován**, lze jej použít k zadávání objednávek call centra a procesy odeslání katalogu.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Použití katalogů k urychlení nacenění a propagace prodejní objednávky

Základním důvodem definování katalogu k použití s call centrem je možnost konfigurovat konkrétní ceny a promoakce pro daný katalog. Zákazníci, kteří objednávají z tohoto katalogu, budou tyto ceny a propagace dostávat v zadání objednávky z call centra v případě, že je v záhlaví nebo řádkách objednávky použito **ID zdrojového kódu**.

Abyste mohli nakonfigurovat katalogové ceny, vyberte možnost **cenové skupiny** na kartě **katalogy** k propojení jedné nebo více cenových skupiny s katalogem. Všechny obchodní smlouvy, deníky úprav cen a rozšířené slevy (prahová hodnota, množství, kombinace a shoda), které byly propojeny se stejnou cenovou skupinou, budou použity, když si zákazníci objednají z tohoto katalogu.

Na pevné záložce **zdrojové kódy** klepněte na tlačítko **přidat** pro přidání jednoho nebo více identifikátorů **ID zdrojového kódu** do tohoto katalogu. Toto je kód, který se použije při zadávání objednávky call centra do záhlaví (a řádků) prodejní objednávky. Tento kód se používá ke spojení prodejní objednávky s katalogem a nakonec pro cenové skupiny a všechny zvláštní ceny nebo promoakce, které byly nakonfigurovány.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>ID zdroje slouží ke sledování nákladů a míry odpovědí

Při definování **ID zdrojového kódu** můžete volitelně propojit toto ID s **ID cílového trhu**. **ID cílového trhu** lze definovat v cestě **Retail and Commerce** \> **Odběratelé** \> **cílový trh**. Cílový trh je seznam odběratelů nebo potenciálních zákazníků náležející do uživatelem definovaného segmentu. Propojení údajů zákazníka nebo potenciálního zákazníka s ID zdrojového kódu umožňuje lepší přehled o příjemcích katalogu. Pokud je zákazník propojen s cílovým trhem a ten je propojen s ID nebo katalogem aktivního zdrojového kódu, budou uživatelé call centra moci podívat, jaké katalogy zákazník přijal, výběrem možnosti nabídky **zdrojové kódy** na kartě **Odběratelé** stránky **odběratelský servis**. Při zadávání objednávky mohou uživatelé call centra rovněž zobrazit konkrétní katalogy zaslané zákazníkovi v rozevíracím seznamu **zdroj** v záhlaví prodejní objednávky. Změna filtru z **všechny** na **Cílené** umožní uživatelům zobrazit konkrétní aktivní katalogy odeslané odběrateli. To je užitečné v situacích, kdy zákazník zapomněl na katalog nebo nemůže najít nebo číst kód katalogu tehdy, kdy volají s žádostí o vytvoření prodejní objednávky.

Je možné propojit více ID zdrojového kódu s katalogem. To je často potřeba, když chce společnost sledovat míru odpovědí podle různých segmentů. Společnost vydá jedinečný kód katalogu jiným zákaznickým segmentům, což umožňuje sledovat množství odpovědí na úrovni segmentu, v rámci konkrétního katalogu události.

Výběr konkrétního záznamu **ID zdrojového kódu** záznam a kliknutí na možnost **podrobnosti** na pevné záložce **zdrojové kódy** poskytuje další pole, které mohou být zaznamenány odhady prodejů, poštovné a poštovní data. Tato data jsou užitečné pro provádění podrobné analýzy efektivnosti katalogu. Uživatelé se mohou k této stránce průběžně vracet a použít tlačítka **zdrojový kód analýzy** a **porovnání promoakcí** k aktivaci analytických sestav založených na aktuálních datech prodeje a k porovnání nákladů a skutečné hodnoty rozpočtu.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Konfigurace objednávky specifické pro katalog a skriptů položek

Když uživatel call centra vytváří prodejní objednávku, může použít skripty na obrazovce. Tyto textové skripty mohou poskytovat doplňující informace, které by uživatel měl sdělit odběrateli nebo to mohou být interní poznámky/upomínky, které by měl uživatel call centra zkontrolovat a reagovat na ně při vytváření prodejní objednávky.

Často je užitečné mít různé sady skriptů pro různé katalogy. Na pevné záložce **skripty** lze propojit předdefinována skripty s katalogem. Pomocí pole **časování** určete, zda se skript zobrazí na začátku objednávky (hned jak je ID zdrojového kódu zadané v záhlaví objednávky) nebo na konci objednávky (v souhrnném formuláři prodejní objednávky).

Při výběru uzel v hierarchii katalogu a práci s daty na pevné záložce **produkty** můžete propojit také skripty, které jsou specifické pro katalogy nebo položky, s použitím akce **skripty**.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Konfigurace nastavení návazného a křížového prodeje zboží z katalogu

Propojení návrhů Návazný/křížový prodej zboží lze provést pomocí nastavení produktů, ale v některých případech může společnost chtít podporovat speciální Návazný/křížový prodej položky k objednání určitého produktu v katalogu specifického odběratele. Na pevné záložce **produkty** vyberte požadovanou položku a klepněte na tlačítko **Návazný/křížový prodej zboží** ke konfiguraci produktů pro prodej odběratelům, kteří nakupují vybrané položky z katalogu. Při zadávání objednávky call centra se určité položky Návazný/křížový prodej katalogu zobrazí na obrazovce, namísto standardních produktů Návazný/křížový prodej, které byly konfigurovány pro danou položku konfigurací obvyklého produktu.

Návazný/křížový prodej zboží také může využívat výhod funkce skriptů pro zobrazení zpráv specifického typu, které uvidí uživatel při zobrazení při zadávání objednávky. Skripty, které jsou vázány na Návazný/křížový prodej produktů konfigurovaný pro produkt v katalogu se zobrazí, pouze pokud zdrojový kód tohoto katalogu se používá v zadávání objednávek call centra.

## <a name="catalog-page-analysis"></a>Analýza stránky katalogu

Na kartě **katalogy** jsou k dispozici možnosti ke konfiguraci **stránek katalogu**. Tato funkce umožňuje definovat specifické stránky a typy stránek pro tištěný katalog a jejich přiřazeny náklady.

Při konfiguraci produktů v katalogu, použijte akci **rozložení stránky produktu** k definování specifických stránek, procenta stránky a pozice detailů stránky pro položku. Konfigurace uživatelům umožňuje využívat **sestavu analýzy oblasti katalogu**. Tuto sestavu lze najít po přechodu do sestavy **Retail and Commerce** \> **Sestavy kontaktního střediska** \> **Analýza oblasti katalogu**. Tato sestava analyzuje prodeje podle katalogu (prodejní objednávky, kde bylo ID zdroje katalogu vázané na záhlaví objednávky nebo řádku prodejní objednávky) a jejich přidružené procento stránky nákladů pro sestavu tradičního přímého marketingu a sestavu **Analýza čtverečních palců**.

## <a name="catalog-requests"></a>Požadavky na katalog

Při konfiguraci a publikování katalogů v aplikaci Commerce lze využít funkci **Odeslat katalog**. Tato funkce je k dispozici na stránce **Hledat zákazníka** a **odběratelský servis**. Po výběru záznamu odběratele pomocí možnosti **Hledat zákazníka** nebo při zobrazení vybraného účtu odběratele vybraný z pole **odběratelský servis**, uživatelé mohou vybrat možnost **odeslání katalogu**, kterou se otevře dialogové okno umožňující uživateli zvolit ze seznamu všech publikovaných a aktivních katalogů. Uživatel může vybrat katalog a množství a konkrétní ID zdrojového kódu k odeslání. Po klepnutí na tlačítko **odeslat** se uloží požadavek, který lze poté spravovat vytištěním sestavy **požadavky na katalogu**. Tuto sestavu lze najít po přechodu do **Retail and Commerce** \> **Sestavy kontaktního střediska** \> **Sestava požadavků katalogu**. Zobrazuje seznam všech požadavků na katalog, včetně názvu a adresy zákazníka, který si vyžádal katalog. Tuto sestavu lze použít interně nebo je možné přenést data třetí straně podporující externí procesy pro fyzické odeslání katalogu odběrateli.

## <a name="additional-features"></a>Další funkce

Na kartě **katalogy** kartě Možnosti konfigurace jsou k dispozici možnosti pro konfiguraci **platebního kalendáře** a **uvolnění produktů**. Pokud je ID zdrojového kódu připojené ke katalogu použito při zadávání objednávky kontaktního střediska, bude odběratel mít nárok na bezplatné produkty nebo použití určitého platebního kalendáře katalogu dle definice. Pokud je nutné omezit odběratele pouze na možnost vybírat platební kalendáře, které jsou spojené s jejich katalogem a ne všemi aktivními platebními kalendáři v systému, lze zaškrtnout políčko **povolit jen plány katalogu** pro jeden nebo více ID zdrojového kódu definované pro vynucení tohoto omezení.

## <a name="additional-notes"></a>Další poznámky

V současné době platí, že když je použito ID zdrojového kódu pro všechny prodejní objednávky v call centru, použije se pro generování cen, promoakcí, skriptů a návazného/křížového prodeje specifických pro katalog. Systém nebude zakazovat ani zabraňovat objednání produktu, který není v katalogu, v prodejní objednávce. Pokud je objednaná položka, která není součástí katalogu, systém použije nejprve **Cenovou skupinu** definovanou v kanálu kontaktního střediska (**Retail and Commerce** \> **Kanály** \> **kontaktní střediska** \> **šechna kontaktní střediska**) pro ceny zboží nebo promoakcí. Pokud žádná konkrétní kanálová cena není nalezena, použije se základní prodejní cena zboží.


[!INCLUDE[footer-include](../includes/footer-banner.md)]