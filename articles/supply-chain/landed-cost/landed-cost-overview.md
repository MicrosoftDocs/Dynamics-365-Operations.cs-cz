---
title: Modul Náklady za doručení
description: Modul Náklady za doručení pomáhá podnikům zefektivnit příchozí přepravní operace tím, že poskytuje uživatelům úplnou finanční a logistickou kontrolu nad importovaným nákladem, od výrobce až po sklad.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccc6f0100582b9703b9755b50b7e8504aa153d15
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022125"
---
# <a name="landed-cost-module"></a>Modul Náklady za doručení

[!include [banner](../../includes/banner.md)]

Modul **Náklady za doručení** pomáhá podnikům zefektivnit příchozí přepravní operace tím, že poskytuje uživatelům úplnou finanční a logistickou kontrolu nad importovaným nákladem, od výrobce až po sklad. U dováženého zboží mohou náklady za doručení představovat 40 procent nebo ještě více z celkových nákladů na každou importovanou položku. Přesné odhady nákladů za doručení jsou proto nesmírně důležité.

Podniky mohou pomocí nákladů za doručení provést následující úkoly:

- Odhadnout náklady za doručení v době vytvoření cesty.
- Rozdělit náklady za doručení mezi více položek a nákupních objednávek nebo převodních příkazů v jedné cestě.
- Podpořit přepravu zboží mezi fyzickými místy identifikací nákladů za doručení.
- Rozpoznat časově rozlišené položky u přepravovaného zboží.

Náklady za doručení poskytují přesné a včasné odhady nákladů na režijní náklady za doručení. Zároveň poskytují lepší finanční a logistický náhled do rozšířeného dodavatelského řetězce. Pomáhá také omezit správu výpočtu nákladů a chyb při stanovení nákladů.

## <a name="highlights"></a>Hlavní body

### <a name="voyages"></a>Cesty

V modulu Náklady za doručení je cesta samostatným pohybem z odchozího místa, procházející přes určitou sadu cílů během zadaného období, až do zadaného umístění příchozího skladu. Nákupní objednávky a řádky objednávek lze u cesty přidat buď do jednoho kontejneru, nebo do více kontejnerů, a náklady budou správně přiděleny zpět do řádku položky. Objednávky a řádky objednávek lze také přidat mezi jednotlivé právnické osoby jedné cesty.

### <a name="item-ownership"></a>Vlastnictví položky

V Microsoftu Dynamics 365 Supply Chain Management je zboží je obvykle přijato v cílovém skladu a poté fakturováno. Podle většiny mezinárodních obchodních dohod však podnik převezme vlastnictví zboží od okamžiku, kdy opustí původní přístav, ještě než bude fyzicky přijato. Náklady za doručení umožňují podnikům fakturovat zboží před jeho fyzickým přijetím. Tento koncept je znám jako objednávka přepravovaného zboží. Vytvoří nový typ objednávky, určený pro správu příjmu zboží po fakturaci původní nákupní objednávky.

### <a name="costs"></a>Náklady

Když v modulu Náklady za doručení vytvoříte cestu, lze k ní automaticky přidat náklady. Tyto náklady jsou nastaveny v modulu Náklady za doručení a jsou pro ně k dispozici různé možnosti nákladů a nákladové základny. Každý náklad může být nastaven pro různé úrovně cesty a rozdělen na úrovni položek pomocí pravidel rozdělení, která podporují množství, objem, hmotnost, částku a definované objemové dělitele. Tyto odhadované náklady poskytují přesný odhad všech nákladů na cestu.

Modul Náklady za doručení poté spustí předběžné zaúčtování / časové rozlišení odhadovaných nákladů za doručení, aby bylo zajištěno, že v době vytvoření cesty bude k dispozici přesný výpočet odhadovaných nákladů. Protože tyto automatické náklady jsou fakturovány, jsou odhadované náklady stornovány a nahrazeny skutečnými náklady na základě nákladových faktur.

Skutečné náklady jsou reverzní odhadované náklady, které jsou zaúčtovány v době fakturace nákladů pomocí clearingových účtů, které jsou nastaveny pro každý typ nákladů (například clo, přepravné a pojištění). Tato účtování dodržují chování účtování, které je přidruženo ke konkrétní položce. Automaticky aktualizují účtování zásob bez ohledu na to, zda je typ účtování první dovnitř, první ven (FIFO), poslední dovnitř, první ven (LIFO), klouzavý vážený průměr nebo klouzavý průměr. Podporovány jsou všechny typy účtování skupin modelů zásob. Pro účtování klouzavých průměrů a standardních nákladů jsou k dispozici účty odchylek nákupních cen, které umožňují zaúčtovat rozdíly mezi odhadovanými a skutečnými náklady.

### <a name="item-and-order-tracking"></a>Sledování položek a objednávek

Jak se cesta pohybuje z původního odchozího místa do konečného cílového skladu, uživatelé mohou aktualizovat každý krok neboli *úsek* cesty podle potřeby. Pro každý úsek je identifikována doba realizace a stav dodávky. Rovněž jsou identifikovány potvrzené termíny dodání pro přesun na další úsek cesty. Společně tato data dodání poskytují odhadované datum dodání zboží do příchozího skladu. Uživatelé mohou tato data dodání změnit. V tomto případě se poté automaticky aktualizuje odhadované datum dodání zboží na základě dob realizace a úseků cesty. Viditelnost zboží při přepravě podle cesty a plavidla je k dispozici na základě jednotlivých kontejnerů před přijetím zboží. Data jsou aktualizována na každém řádku nákupní objednávky, a proto mají podniky větší kontrolu nad logistikou a plánováním skladu.

## <a name="landed-cost-concepts"></a>Koncepty nákladů za doručení

Následující tabulka shrnuje některé klíčové koncepty modulu Náklady za doručení.

| Koncept | Popis |
|---|---|
| Cesta | Cesta je obvykle jedno plavidlo. V závislosti na vašich zvycích a postupech to však může být jeden prodejce nebo jedna nákupní objednávka. Použití tohoto konceptu není nijak omezeno. |
| Folio | Folio je často určeno celní předpisy. Může se skládat ze zboží jednoho dodavatele pro jednu entitu / společnost na zásilku. Zboží ve foliu může být v jednom kontejneru nebo rozloženo mezi více kontejnerů. |
| Přepravní kontejner | Přepravní kontejnery ukládají řádky objednávek. Jsou o úroveň níže než úroveň zásilky. Obvykle se používají, pokud jsou náklady rozděleny na zboží podle kontejneru nebo pokud se příjem provádí podle kontejneru. |
| Typ přepravního kontejneru | Typy přepravních kontejnerů mohou určit cenu pro typ nákladů (například přepravné). Poskytují také užitečné informace o přepravě. |
| Typ nákladů | Typy nákladů identifikují náklady spojené s dovozem, jako je clo, přepravné a pojištění. |
| Automatické náklady | Automatické náklady fungují jako obchodní smlouvy. Automatický náklad je spojen s úrovní cesty. |
| Přístav | Přístavy jsou oblasti, ve kterých je zboží přijímáno a odkud je přepravováno. |
| Plavidlo | Plavidlo je médium, které se používá k přepravě zboží, například loď nebo letadlo. |
| Přepravované zboží | V závislosti na nastavení se zboží po aktualizaci faktury vloží do tranzitního skladu. |
| Aktivita | Aktivity lze použít k uložení každého významného kroku cesty mezi dvěma přístavy. Lze je použít k aktualizaci dat. |
| Šablona cesty | Šablony cest jsou trasy, kterými zboží cestuje mezi dvěma přístavy. |

Pro srovnání terminologie a vlastností modulů **Náklady za doručení** a **Správa přepravy** (TMS) najdete v tématu [Náklady za doručení vs. Správa přepravy](landed-cost-vs-tms.md).
