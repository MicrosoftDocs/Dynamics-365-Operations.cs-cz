---
title: Přehled konfigurace skladu
description: Tento článek popisuje konfiguraci skladu. Obsahuje informace o postupu při povolení rozvržení skladu a procesů skladu.
author: perlynne
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1dc6c99a986bad767691f7cac7e0135c54e1d0b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189544"
---
# <a name="warehouse-configuration-overview"></a>Přehled konfigurace skladu

[!include [banner](../includes/banner.md)]

Tento článek popisuje konfiguraci skladu. Obsahuje informace o postupu při povolení rozvržení skladu a procesů skladu.

> [!NOTE]
> Tento článek se vztahuje k funkcím v modulu **Řízení skladu** (pokročilé uskladnění). Nevztahuje se na funkce skladu v modulu **Řízení zásob**.

## <a name="warehouse-layout"></a>Rozvržení skladu
Systému správy skladu v aplikaci Supply Chain Management umožňuje flexibilní způsoby definování rozvržení skladu podle měnících se potřeb, aby bylo možné dosáhnout optimální efektivity skladu.

-   Je možné vytvořit úložné prostory vysoké a nízké priority pro optimální umístění zboží.
-   Sklad lze rozdělit do zón a přizpůsobit je různým požadavkům na skladování, jako je například teplota či různé sazby obratu pro zboží.
-   Skladová místa lze specifikovat na kterékoli úrovni (například pracoviště, sklad, ulička, stojan, police a přihrádka).
-   Umístění lze seskupit pomocí nastavení fyzických omezení kapacity.
-   Můžete řídit způsob skladování a výdeje zboží podle pravidel definovaných dotazem.

Chcete-li použít správu skladu v aplikaci Supply Chain Management, musíte vytvořit skladu a povolit jej pro pokročilejší nebo specializovanější aktivity správy skladu. Na stránce **Sklady** vyberte možnost **Použít procesy správy skladu**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Skupiny zón, zóny, typy skladových míst a skladová místa

V rámci procesu povolení rozvržení skladu je nutné definovat skupiny zón skladu, zóny, profily skladových míst, typy skladových míst a skladová místa.

-   **Skupiny zón** – Logické či fyzické seskupení zón ve skladu.
-   **Zóny** – Logické či fyzické seskupení skladových míst ve skladu.
-   **Profily umístění** – Logické či fyzické seskupení skladových míst, které mají stejné zásady procesů skladových míst (například zde mohou být uloženy kombinace různých čísel položek a platí stejná fyzická omezení kapacity).
-   **Typy skladových míst** – Logické či fyzické seskupení skladových míst ve skladu. Můžete například vytvořit typ skladového místa pro všechna přechodná skladová místa. Povinná nastavení na stránce **Parametry správy skladu** řídí proces stanovení typu přechodných skladových míst a typ konečného skladového místa.
-   **Místa** – Nejnižší úroveň informací o skladovém místě. Místa se používají ke sledování toho, kde budou zásoby na skladě uloženy a vyzvednuty ve skladu.

Entity, které vytvoříte k definování rozvržení skladu, se používají v dotazech, které nastavíte v šablonách práce a které řídí pracovní zakázky ve skladu. Proto definujte zóny, typy skladových míst a tak dále a zvažte, jak se různé oblasti ve skladu postupy používají pro různé postupy. Dále zvažte faktory, jako jsou například fyzické vlastnosti konkrétní oblasti. Například mohou existovat místa, kde lze použít pouze určitý typ vysokozdvižného vozíku. Nebo pokud vaše společnost má výrobu a hotové výrobky v rámci stejného zařízení, můžete vytvořit jeden sklad v aplikaci Supply Chain Management, ale pak můžete tyto dvě operace oddělit vytvořením dvou skupin zón. Zadejte pro entity popisné názvy, aby bylo možné je snadno identifikovat při použití v dotazech šablony.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Limity skladových míst, profily skladových míst a pevná výdejní místa

Je nutné zvážit fyzické rozvržení skladu, za účelem určení kapacity úložiště (limity skladových míst a profily skladových míst) a v rámci vašich pokusů za účelem dosažení optimálních skladových procesů. 

Díky limitům pro místo uskladnění se nevytvoří práce vyžadující umístění zásob na skladové místo, které nemá pro zásoby fyzickou kapacitu. Pokud například některá umístění ve skladu pojmou pouze jednu paletu na umístění, můžete povolit limity pro místo uskladnění. Hodnotu **Množství** lze nastavit na **1** a hodnotu **Jednotka** lze nastavit na **PL** v rámci určitého seskupení profilů skladového místa. 

Pokud řízení omezení kapacity skladového místa vyžaduje rozšířené výpočty, lze použít nastavení profilu skladového místa. V takovém případě je zvážena hmotnost a objem při provádění výpočtů kapacity. 

K dosažení optimálních výstupních procesů byste měli vyhodnotit, zda mají být použita pevná výdejní skladová místa nebo skladová místa pro balení. Často se hodnoty minimálního nebo maximálního doplnění používají pro procesy doplnění ze skladové oblasti do pevných výdejních skladových míst a několik pevných výdejních skladových míst lze povolit ve stejném skladu a pro varianty produktu. Zvažte flexibilitu, které byste mohli dosáhnout povolením vyhrazených skladových míst v případě přeplnění na vyžádání, která se používají pouze pro zpracování vlny doplnění / vytížení.

### <a name="location-setup-wizard"></a>Průvodce nastavením skladového místa

Chcete-li rychle vytvořit skladová místa ve skladu, můžete použít průvodce **nastavením skladového místa**. Jako součást tohoto postupu můžete snadno uchovávat formát názvů skladového místa.

## <a name="warehouse-processes"></a>Skladové procesy
V rámci konfigurace skladu je důležité povolit procesy skladu podle obchodních požadavků. Nejdůležitější součásti, které je třeba nakonfigurovat, jsou šablony vlny, šablony práce, fondy práce a směrnice skladového místa.

### <a name="wave-templates"></a>Šablony vlny

Šablony vlny pomáhají povolit odchozí proces "Uvolnění do skladu". Po uvolnění řádků objednávky (buď přímo ze zdrojových dokumentů, pomocí dávkových procesů úloh nebo pomocí zatížení, které již bylo vytvořeno), se používá funkce šablony vlny. 

Můžete vytvářet tři typy šablon vlny: 
-   **Expedice**
-   **Výrobní zakázka**
-   **Kanban** 

Parametry se používají k definování, co může systém automaticky provést při zpracování odchozí práce. Šablona vlny je vybrána na základě pořadí šablony vlny a kritérií, která jsou zadána v šabloně. Pokud je šablona uvedena v horní části řady, jsou nejprve zkontrolována kritéria v této šabloně. Pokud kritéria nelze splnit, bude zpracována šablona vlny. V opačném případě budou zkontrolována kritéria v další šabloně a tak dále. Je proto vhodné vložit šablonu, která obsahuje nejkonkrétnější kritéria, do horní části seznamu pořadí šablon vlny, aby byla zpracována jako první. Například chcete zpracovat všechnu dnešní práci konkrétního dopravce a dočasně odložit zpracování práce pro ostatní dopravce. V tomto případě by měla být šablona vlny, která vybere práci pro daného dopravce, uvedena v pořadí výše než jiné šablony. V opačném případě může být práce ostatních dopravců zpracována před dokončením práce daného dopravce. 

V každé šabloně vlny je nutné zadat metody zpracování vlny. Metody, které jsou k dispozici, se liší v závislosti na typu šablony vlny.

### <a name="work-templates"></a>Šablony práce

Definice šablon vlny hrají důležitou roli v definici pracovních procesů řízení skladu. Definují, jaké práce se provádí, a jak. Šablony mohou rovněž obsahovat kód směrnice odkazující na směrnici skladového místa, podle které lze určit, kde se práce provádí. Šablony práce zahrnují dotaz, který určuje kritéria pro práci. Každá šablona musí obsahovat alespoň jednu operaci výdeje a jednu operaci vložení, která řídí základní operaci práce převedení zásob na skladě z jednoho místa do druhého. 

Pokud je nutné, aby více zaměstnanců zpracovalo práci pro některé operace skladu, můžete chtít použít koncept *fázování* zásob a rozdělit vykonání práce v různých pracovních třídách.

### <a name="work-pools"></a>Fondy práce

Fondy práce se používají k uspořádání práce do skupin. Můžete například vytvořit fond práce pro klasifikaci práce, ke které dochází v určitém skladovém místě. Pro všechny typy prací s výjimkou počítání můžete přiřadit fond práce k šabloně práce. Pro cyklickou inventuru můžete přiřadit fond práce na následujících stránkách:

-   Plány cyklických inventur
-   Prahové hodnoty cyklické inventury
-   Práci cyklické inventury podle skladového místa
-   Práce cyklické inventury podle zboží

Používáte-li pracovní šablony k vytváření práce, fond práce je automaticky přiřazen k práci. 

ID fondu práce rovněž slouží k omezení druhu práce, která je určena pro určitého pracovníka skladu, pokud je tato funkce nakonfigurována v položce nabídky příslušného mobilního zařízení.

### <a name="location-directives"></a>Směrnice skladového místa

Jako název naznačuje, směrnice skladového místa slouží ke směrování pracovních transakcí do příslušných skladových míst ve skladu. Jinak řečeno určují, kde probíhá výdej a uložení. 

Chcete-li usnadnit a urychlit definování akcí, které jsou přidruženy k jednotlivým řádkům směrnice skladového místa, použijte jednu z předdefinovaných strategií. Můžete například použít strategii **Prázdné umístění s žádnou příchozí prací** k vyhledávání volného místa ve skladu, nebo můžete použít strategii **Rezervace dávky FEFO** pro odchozí výdej prodeje.

## <a name="additional-resources"></a>Další zdroje

[Konfigurace umístění ve skladu s povolenými procesy řízení skladu](tasks/configure-locations-wms-enabled-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]