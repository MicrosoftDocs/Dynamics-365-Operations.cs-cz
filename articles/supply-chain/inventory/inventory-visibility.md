---
title: Přehled doplňku Inventory Visibility
description: Tento článek vysvětluje, co je Viditelnost zásob a popisuje funkce doplňku.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066633"
---
# <a name="inventory-visibility-add-in-overview"></a>Přehled doplňku Viditelnost zásob

[!include [banner](../includes/banner.md)]

Doplněk Viditelnost zásob (označovaný také jako *služba Viditelnost zásob*) poskytuje nezávislou a vysoce škálovatelnou mikroslužbu, která umožňuje okamžité účtování změn zásob v reálném čase a sledování viditelnosti napříč všemi vašimi datovými zdroji a kanály. Poskytuje platformu, která vám umožní spravovat vaše globální zásoby pomocí funkcí, které zahrnují (ale nejen) následující seznam:

- Centrální sledování nejnovějšího stavu zásob (například na skladě, objednané, zakoupené, na cestě, vrácené a v karanténě) napříč všemi datovými zdroji, sklady a umístěními připojením aplikace Supply Chain Management nebo zdrojů logistických dat třetích stran (jako jsou systémy pro správu objednávek, systémy \[ERP\] plánování podnikových zdrojů třetích stran, systémy pokladních míst \[POS\] a systémy řízení skladu) ke službě Viditelnost zásob.
- Dotazy na dostupnost zboží na skladě a nedostatek zásob, a získání okamžité odpovědi přímým voláním služby Viditelnost zásob.
- Eliminace nadměrného prodeje, zvláště když vaše poptávka pochází z různých kanálů, pomocí předběžných rezervací v reálném čase ve službě Viditelnost zásob.
- Lepší správa slíbených objednávek a očekávání zákazníků poskytnutím přesných dat o aktuální nebo následující dostupnosti, aby funkce Omnikanálu Lze slíbit (ATP) mohla vypočítat očekávaná data plnění objednávek.

## <a name="extensibility"></a>Rozšiřitelnost

Služba Viditelnost zásob je rozšiřitelná, protože vstup a výstup dat není omezen na aplikace společnosti Microsoft. Externí systémy mohou přistupovat ke službě prostřednictvím RESTful aplikačních programovacích rozhraní (API). Kromě použití předem připravených mapování, která jsou k dispozici pro zdroj dat a dimenze Supply Chain Management, můžete integrovat Viditelnost zásob s různými systémy třetích stran nastavením dalších zdrojů dat, měr stavů zásob (označovaných ve službě Viditelnost zásob jako *fyzické míry*) a dimenzí inventáře prostřednictvím konfigurační aplikace. Tímto způsobem můžete flexibilně dotazovat a měnit své různé zdroje dat a předdefinované dimenze zásob.

Navíc, protože služba Viditelnost zásob používá Microsoft Dataverse, lze její data použít k sestavení a integraci s Power Apps. Power BI můžete také použít k vytvoření přizpůsobených řídicích panelů, které splňují vaše obchodní požadavky.

## <a name="scalability"></a>Škálovatelnost

Službu Viditelnost skladu lze škálovat nahoru nebo dolů v závislosti na objemu vašich dat. Škálovatelnost je většinou bezproblémová a je řízena týmem platformy Microsoft na základě automatické detekce a vyhodnocení objemu vašich transakčních dat.

## <a name="feature-highlights"></a>Zvýrazněné funkce

### <a name="get-a-global-view-of-real-time-inventory"></a>Jak získat globální přehled o zásobách v reálném čase

Viditelnost zásob zajišťuje, že budete mít kdykoli přístup k nejaktuálnějším množstvím zásob ve všech vašich kanálech, místech a skladech. Nejvíce budete těžit z toho, že službu budete používat k podpoře vašeho každodenního provozního podnikání, kdykoli potřebujete získat záznamy o zásobách. Fyzické zásoby na skladě, prodaná a zakoupená množství jsou automaticky k dispozici. Můžete také konfigurovat další fyzické míry zásob (jako jsou data o vráceném zboží, zboží v karanténě a odeslaném zboží), jak potřebujete, abyste získali tyto podrobnosti v reálném čase. Viditelnost zásob dokáže efektivně zpracovat miliony zaúčtovaných změn zásob. Tato data lze agregovat a promítnout do nejnovějších zásob ve službě okamžitě, za sekundu nebo za minutu, v závislosti na intervalu, ve kterém jsou data zaúčtována. Další informace viz [Veřejná rozhraní API Viditelnosti zásob](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Předběžná rezervace, která brání nadměrnému prodeji ve všech kanálech objednávek

*Předběžná rezervace* umožňuje přiřadit nebo označit konkrétní množství pro splnění objednávky nebo poptávky. Předběžná rezervace neovlivňuje fyzické zásoby, ale odečítá z nich množství zásob *k dispozici pro rezervaci* a poskytuje aktualizované množství pro budoucí plnění objednávky. Tato funkce je užitečná, pokud do vašeho podniku přicházejí prodejní požadavky nebo objednávky z jednoho nebo více kanálů nebo zdrojů dat, které jdou mimo váš systém plánování podnikových zdrojů (ERP).

Pokud nepoužíváte předběžné rezervace ve službě Viditelnost zásob, musíte počkat, dokud nebude objednávka synchronizována a zpracována vaším systémem ERP, abyste získali aktualizaci fyzického množství zásob. Tento proces má obvykle velkou latenci. Předběžné rezervace se však okamžitě projeví pokaždé, když je ve vašich prodejních kanálech vygenerována prodejní žádost nebo objednávka. Pomáhají tedy předcházet situacím nadměrného prodeje tím, že zajišťují, aby se vaše objednávky v Omnikanálu vzájemně nerušily, když se nakonec dostanou do ERP systému. Předběžné rezervace také zajišťují, že můžete splnit všechny objednávky, které jste slíbili. Pomohou vám tedy splnit očekávání zákazníků a udržet jejich loajalitu. Další informace viz [Rezervace ve Viditelnosti zásob](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Okamžitá odpověď na potvrzení dat ATP

Viditelnost vašich předpokládaných zásob v blízké budoucnosti (včetně nabídky, poptávky a předpokládaných podrobností o množství na skladě) je důležitá, protože pomáhá vaší společnosti dosáhnout následujících cílů:

- Minimalizovat úrovně zásob, abyste snížili náklady na jejich správu.
- Usnadnit interní zpracování objednávek, aby prodejci mohli vypočítat data odeslání a dodání na základě dostupnosti objednaných produktů.
- Poskytovat transparentní informace o tom, kdy mohou zákazníci očekávat, že položka není skladem, a to uvedením nejbližšího data dostupnosti.

Funkci ATP lze snadno zařadit do vašeho každodenního procesu vyřizování objednávek. A co je nejdůležitější, stejně jako ostatní funkce Viditelnosti zásob je i ATP *globální a v reálném čase*. Proto můžete nastavit více vzorců pro výpočet ATP, abyste měli úplné dotazy na dostupnost zásob, které pokrývají všechny vaše obchodní kanály a zdroje dat. Další informace najdete v tématu [Plány změn ve skladu Viditelnosti zásob a funkce Lze slíbit](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>Kompatibilita s položkami procesů správy skladu (WMS)

Cílem společnosti Microsoft je poskytnout okamžitou integraci s procesy správy skladu (WMS), aby zákazníci WMS mohli také využívat výhod služby Viditelnost zásob. Ve vlně 1 vydání 2022 (veřejné preview v březnu) služba zásob podporuje dotazy na položky WMS a ATP. Funkce předběžné rezervace a přidělování bude pro zákazníky WMS podporována v příští vlně. Další informace viz [Podpora Viditelnost zásob pro položky WMS](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Licence

Služba Viditelnost zásob je k dispozici v následujících verzích:

- **Doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management** – Pro společnosti, které mají platnou licenci Supply Chain Management, je Viditelnost zásob k dispozici bez dalších licenčních nákladů. Můžete ji hned začít zkoušet. Podrobnosti o instalaci najdete v tématu [Instalace a nastavení viditelnosti zásob](inventory-visibility-setup.md).
- **Služba Viditelnosti zásob jako součást IOM** – Tato verze je určena buď pro zákazníky Intelligent Order Management (IOM), nebo pro společnosti, které nepoužívají Supply Chain Management jako svůj ERP systém. Licence je součástí balíčku IOM. Další informace naleznete v tématu [Přehled aplikace Intelligent Order Management](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
