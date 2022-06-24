---
title: Komponenty elektronického výkaznictví
description: Tento článek popisuje komponenty elektronického výkaznictví (ER).
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2b8b197fdea0cd49fc5161a12b8f547cc1a27bf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892443"
---
# <a name="electronic-reporting-components"></a>Komponenty elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Elektronické výkaznictví (ER) podporuje následující typy komponent:

- Datový model
- Mapování modelu
- Formát
- Metadata

## <a name="data-model-component"></a>Komponenta datového modelu

Komponenta datového modelu je abstraktní reprezentací datové struktury. Popisuje konkrétní oblast obchodní domény s dostatečným množstvím podrobností, aby byly splněny požadavky na výkazy pro tuto doménu. Součást modelu dat se skládá z následujících částí:

- **Datový model** – Sada obchodních entit konkrétní domény a hierarchicky strukturované definice vztahů mezi nimi.
- **Mapování modelu** – Vybrané zdroje dat aplikace jsou spojeny s jednotlivými prvky datového modelu, který při spuštění určuje tok dat a pravidla zadávání obchodních dat do komponenty modelu dat.

Obchodní entita modelu dat je vyjádřena jako kontejner nebo záznam. Vlastnosti obchodní entity jsou reprezentovány položkami dat nebo poli. Každá datová položka má jedinečný název, štítek, popis a hodnotu. Hodnota pro každou datovou položku může být určena tak, aby byla rozpoznána jako řetězec, celé číslo, reálné číslo, datum, výčet nebo logická hodnota. Kromě toho může být datová položka jiným záznamem nebo seznamem záznamů.

Jedna komponenta datového modelu může obsahovat několik hierarchií obchodních entit pro konkrétní doménu. Může také obsahovat mapování modelu, která podporují v operačním čase tok dat pro konkrétní sestavu. Hierarchie se mohou lišit podle jednotlivých záznamů, které jsou vybrány jako kořen mapování modelu. Například datový model oblasti domény platby může podporovat následující mapování:


- Společnost \> Dodavatel \> Platební transakce domény závazků
- Zákazník \> Společnost \> Platební transakce pohledávek domény

Obchodní entity, například společnost a platební transakce, jsou určeny pouze jednou. Různá mapování je mohou podle potřeby znovu použít.

## <a name="model-mapping-component"></a>Komponenta mapování modelu

Mapování modelu spojuje zdroje dat aplikace s jednotlivými prvky datového modelu, které při spuštění určují tok dat a pravidla zadávání obchodních dat do komponenty modelu dat.

Mapování modelu, které podporuje odchozí elektronické dokumenty, má tyto funkce:

- Může využívat různé typy dat aplikace jako zdroje dat pro datový model. K těmto datovým typům patří tabulky, datové entity, metody a výčty.
- Podporuje vstupní parametry uživatele lze definovat jako datové zdroje modelu dat, když je při spuštění nutné zadat některá data.
- Podporuje transformaci dat do požadovaných skupin. Umožňuje také filtrování, řazení a sčítání dat a připojování logických vypočítaných polí určených pomocí vzorců podobně jako v aplikaci Microsoft Excel. Další informace najdete v tématu [Návrhář receptur elektronického výkaznictví (ER)](general-electronic-reporting-formula-designer.md).

Mapování modelu, které podporuje příchozí elektronické dokumenty, má tyto funkce:

- Může používat různé aktualizovatelné datové prvky jako cíle. K těmto datovým prvkům patří tabulky, datové entity a zobrazení. Data lze aktualizovat pomocí dat z příchozích elektronických dokumentů. V jednom mapování modelu lze použít více cílů.
- Podporuje vstupní parametry uživatele lze definovat jako datové zdroje modelu dat, když je při spuštění nutné zadat některá data.

Komponenta datového modelu je navržena pro každou obchodní doménu, která se používá jako jednotný zdroj dat pro vykazování. Jednotný zdroj dat izoluje vykazování od fyzické implementace zdrojů dat. Komponenta představuje obchodní koncepce a funkce konkrétní domény ve formě, která zvyšuje efektivitu úvodní struktury formátu výkaznictví a usnadňuje jeho další údržbu.

## <a name="format-component"></a>Komponenta formátu

### <a name="format-components-for-outgoing-electronic-documents"></a>Komponenty formátu pro odchozí elektronické dokumenty

Komponenta formátu je schématem výstupu vykazování, který je generován za běhu aplikace. Schéma se skládá z následujících prvků:

- Formát, který definuje strukturu a obsah odchozího elektronického dokumentu (generuje se za běhu aplikace).
- Zdroje dat jako sada vstupních parametrů uživatele a datového modelu konkrétní domény s mapováním vybraného modelu.
- Formát mapování jako sada vazeb datových zdrojů formátu s jednotlivými prvky formátu, které určují za běhu aplikace tok dat a pravidla generování výstupu formátu.
- Ověření formátu jako sada konfigurovatelných pravidel, která řídí vytváření sestav za běhu aplikace v závislosti na aktuálním kontextu. Může napříkad existovat pravidlo, které zastaví generování výstupu plateb dodavatele dodavatele a vytvoří výjimku, když chybí konkrétní atributy dodavatele, například číslo bankovního účtu.

Komponenta formátu podporuje následující funkce:

- Vytvoření výstupní sestavy jako samostatných souborů v různých formátech, například text, XML, dokument aplikace Microsoft Word nebo sešit
- Vytvoření více souborů samostatně a jejich uložení do souborů ZIP

Komponenta formátu umožňuje připojit určité soubory, které lze použít ve výstupním vykazování:

- Listy sešitů Excel obsahující listy, které lze použít jako šablonu pro výstup ve formátu listu OPENXML
- Soubory aplikace Word obsahující dokument, který lze použít jako šablonu pro výstup ve formátu dokumentu aplikace Microsoft Word
- Ostatní soubory, které mohou být zahrnuty do výstupního formátu jako předdefinovaných souborů

Následující obrázek znázorňuje tok dat u těchto formátů.

[![Tok dat pro odchozí komponenty formátu](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Chcete-li spustit jednu konfiguraci formátu ER a vygenerovat odchozí elektronický dokument, je nutné určit mapování konfigurace formátu.

#### <a name="format-components-for-incoming-electronic-documents"></a>Komponenty formátu pro příchozí elektronické dokumenty
Komponenta formátu je schématem příchozího dokumentu, které se importuje při spuštění. Schéma se skládá z následujících prvků:

- Formát, který definuje strukturu a obsah příchozího elektronického dokumentu obsahujícího data, která se importují při spuštění. Komponenta formátu, která slouží k analýze příchozích dokumentů v různých formátech (například text nebo XML).
- Mapování formátu, které spojuje jednotlivé prvky formátu s prvky datového modelu konkrétní domény. Při spuštění prvky v datovém modelu určují tok dat a pravidla pro import dat z příchozího dokumentu a následně ukládají data do datového modelu.
- Ověření formátu jako sada konfigurovatelných pravidel, která řídí import dat v době spuštění v závislosti na aktuálním kontextu. Může napříkad existovat pravidlo, které zastaví import dat bankovního výpisu s platbami dodavatele a vytvoří výjimku, když chybí konkrétní atributy dodavatele, například jeho identifikační číslo.

Následující obrázek znázorňuje tok dat u těchto formátů.

[![Tok dat pro příchozí komponenty formátu](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Chcete-li spustit jednu konfiguraci formátu ER při importu dat z příchozího elektronického dokumentu, je nutné určit požadované mapování konfigurace formátu a bod integrace mapování modelu. Pro různé typy příchozích dokumentů můžete použít stejné mapování modelu a cíle společně s různými formáty.


## <a name="component-versioning"></a>Správa verzí komponent

Komponenty EV podporují správu verzí je podporována. Následující workflow je určen pro správu změn v komponentách ER:

1. Původně vytvořená verze je označena jako verze **Koncept**. Tato verze může být upravena a je k dispozici pro zkušební běh.
2. Verzi **Koncept** lze převést na verzi **Dokončeno**. Tuto verzi lze použít v místních procesů vykazování.
3. Verzi **Dokončeno** lze převést na verzi **Sdíleno**. Tato verze je publikována ve službě Microsoft Dynamics Lifecycle Services (LCS) a lze ji použít v globálních procesech vykazování.
4. Verzi **Sdíleno** lze převést na verzi **Vyřazeno**. Tuto verzi můžete odstranit.

Verze ve stavu **Dokončeno** nebo **Sdíleno** jsou k dispozici pro další výměnu dat. U komponenty s těmito stavy můžete provádět následující akce:

- Komponentu lze serializovat do formátu XML a exportovat jako soubor ve formátu XML.
- Komponentu lze reserializovat ze souboru XML a importovat do aplikace jako novou verzi komponenty ER.

## <a name="component-date-effectivity"></a>Datum platnosti komponenty

Verze komponent ER platí k určitému datu. Určením hodnoty data „Platné od“ lze u komponenty ER určit datum, kdy komponenta začne platit v procesech vykazování. Datum relace aplikace slouží k definování, zda komponenta je platná pro spuštění. Poslední verze slouží k procesu vykazování při více než jedné platné verzi pro konkrétní datum.

## <a name="component-access"></a>Přístup komponent

Přístup ke komponentám formátu ER závisí na nastavení kódu země/oblasti Mezinárodní organizace pro normalizaci (ISO). Pokud je toto nastavení pro vybranou verzi konfigurace formátu prázdné, k součásti formátu lze přistupovat z libovolné společnosti v době běhu. Pokud toto nastavení obsahuje ISO kódy země/oblasti, je komponenta formátu přístupná pouze ze společností, jejichž primární adresa je definována pro jednu komponentu formátu ISO kódu země/oblasti.

Různé verze součástí formátu data mají pravděpodobně různá nastavení ISO kódů země/oblasti.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

