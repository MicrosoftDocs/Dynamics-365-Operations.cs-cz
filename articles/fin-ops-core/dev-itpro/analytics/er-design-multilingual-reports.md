---
title: Navrhujte vícejazyčné zprávy v elektronickém výkaznictví
description: Toto téma vysvětluje, jak můžete pomocí štítků elektronického výkaznictví (ER) navrhovat a generovat vícejazyčné zprávy.
author: NickSelin
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5a2e8cca441189020e6274248a48c5e9dd80e00
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753545"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Navrhujte vícejazyčné zprávy v elektronickém výkaznictví

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Jako podnikový uživatel můžete používat [architekturu elektronického výkaznictví](general-electronic-reporting.md) ke konfiguraci formátů pro odchozí dokumenty, které musí být generovány v souladu s právními požadavky různých zemí či oblastí. Pokud tyto požadavky vyžadují, aby odchozí dokumenty byly generovány v různých jazycích pro různé země nebo regiony, můžete nakonfigurovat jeden [formát](general-electronic-reporting.md#FormatComponentOutbound) ER, který obsahuje zdroje závislé na jazyce. Tímto způsobem můžete znovu použít formát ke generování odchozích dokumentů pro různé země nebo regiony. Možná budete také chtít použít jediný formát ER k vygenerování odchozího dokumentu v různých jazycích pro odpovídající zákazníky, prodejce, dceřiné společnosti nebo jiné strany.

Datové modely a mapování modelů ER můžete nakonfigurovat jako zdroje dat konfigurovaných formátů ER a definovat tok dat, který určuje, jaká aplikační data se vkládají do generovaných dokumentů. Jako [poskytovatel](general-electronic-reporting.md#Provider) konfigurace ER můžete [publikovat](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) nakonfigurované [datové modely](general-electronic-reporting.md#data-model-and-model-mapping-components), [modelování map](general-electronic-reporting.md#data-model-and-model-mapping-components) a [formáty](general-electronic-reporting.md#FormatComponentOutbound) jako komponenty řešení ER pro generování specifických odchozích dokumentů. Můžete také dovolit zákazníkům [nahrát](general-electronic-reporting-manage-configuration-lifecycle.md) publikované řešení ER tak, aby mohlo být použito a přizpůsobeno. Pokud očekáváte, že zákazníci budou mluvit jinými jazyky, můžete nakonfigurovat komponenty ER tak, aby obsahovaly prostředky závislé na jazyce. Tímto způsobem může být obsah editovatelné komponenty ER prezentován v uživatelsky preferovaném jazyce zákazníka v době návrhu.

Zdroje závislé na jazyce můžete nakonfigurovat jako štítky ER. Tyto štítky pak můžete použít ke konfiguraci součástí ER pro následující účely:

- V době návrhu:

    - Prezentujte obsah nakonfigurovaných komponent ER v uživatelsky preferovaném jazyce.

- Za běhu:

    - Vytvářejte obsah závislý na jazyce pro odchozí dokumenty.
    - Poskytujte varovné a chybové zprávy v uživatelsky preferovaném jazyce.
    - Vyžádejte si požadovaná pole v uživatelském jazyce.

Štítky ER lze konfigurovat v každé [konfiguraci](general-electronic-reporting.md#Configuration) ER, která obsahuje různé komponenty. Štítky mohou být udržovány nezávisle na nakonfigurované logice datových modelů ER, mapování modelů ER a komponent formátů ER.

Každý štítek ER je identifikován pomocí ID, které je jedinečné v rozsahu konfigurace ER, která drží tento štítek. Každý štítek může obsahovat text štítku pro každý jazyk, který je podporován v aktuální instanci Microsoft Dynamics 365 Finance. Tyto podporované jazyky zahrnují jazyky implementovaných vlastních nastavení.

## <a name="entry"></a>Zápis

Když navrhujete datový model ER, mapování modelu ER nebo formát ER, volba **Přeložit** se zobrazí pokaždé, když vyberete pole, které by mohlo obsahovat překladatelný kontext. Pokud vyberete tuto možnost, můžete vybrané pole propojit s ER štítkem v <a name="TextTranslationPane">podokně</a> **Překlad text**. Můžete si vybrat existující označení ER nebo přidat nové označení ER, pokud ještě není k dispozici. Když vyberete nebo přidáte označení ER, můžete přidat související text pro každý jazyk, který je podporován v aktuální instanci Finance.

Následující obrázek ukazuje, jak se tento překlad provádí v upravitelném datovém modelu ER. V tomto příkladu atribut **Popis** pole **Nákupní objednávka** pro editovatelný **Fakturační model** je přeložen do rakouské němčiny (DE-AT) a japonštiny (JA).

![Zajištění překladu značky ER v návrháři datového modelu ER](./media/er-multilingual-labels-refer.png)

Lze přeložit pouze text štítků pro štítky, které se nacházejí v upravitelné komponentě ER. Pokud například vyberete **Přeložit** pro atribut popisku zdroje dat mapování modelu ER a poté vyberete štítek ER, který se nachází v nadřazeném datovém modelu ER, uvidíte obsah štítku, ale nemůžete jej změnit. V těchto případech pole **Přeložený text** není k dispozici, jak ukazuje následující obrázek.

![Kontrolan překladu štítku ER v návrháři mapování modelu ER](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Nemůžete použít návrháře k odstranění štítku, který byl vložen do editovatelné komponenty ER.

## <a name="scope"></a>Rozsah

Označení ER lze označit několika přeložitelnými atributy komponent ER.

### <a name="data-model-component"></a>Komponenta datového modelu

Když konfigurujete datový model ER, můžete pro něj přidat označení ER. Atributy **Štítek** a **Popis** položky modelu, pole každého modelu a každá hodnota <a id="LinkModelEnum"></a>výčtu modelu může být spojena se značkou ER, která je přidána do datového modelu ER.

![Zajištění překladu atributu Popis v návrháři datového modelu ER](./media/er-multilingual-labels-refer.png)

Když je datový model ER nakonfigurován tímto způsobem, jeho obsah bude představen uživatelům návrháře datového modelu ER v preferovaném jazyce každého uživatele. Proto je údržba modelu zjednodušena. Následující obrázky ukazují, jak tato funkce funguje pro uživatele, kteří mají nastavený jazyk DE-AT a JA.

![Rozvržení návrháře datového modelu ER pro uživatele, který má jako preferovaný jazyk nastaven DE-AT](./media/er-multilingual-labels-refer-de.png)

![Rozvržení návrháře datového modelu ER pro uživatele, který má jako preferovaný jazyk nastaven JA](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Komponenta mapování modelu

Protože mapování modelu ER je založeno na datovém modelu ER, popisky prvků datového modelu, na které se odkazuje, se objevují v preferovaném jazyce uživatele v návrháři modelového mapování. Následující obrázek ukazuje, jak je význam pole **Nákupní objednávka** vysvětlen v mapování upravitelného modelu pomocí označení atributu **Popis**, který byl přidán do konfigurovaného datového modelu. Všimněte si, že tento štítek je uveden v preferovaném jazyce uživatele (v tomto příkladu DE-AT).

![Rozvržení návrháře mapování modelu ER pro uživatele, který má jako preferovaný jazyk nastaven DE-AT](./media/er-multilingual-labels-show-mapping.png)

Když je atribut **Štítek** datového zdroje **Vstupní parametr uživatele** nakonfigurován tak, že je spojen se štítkem ER, pole parametrů, které odpovídá tomuto zdroji dat, je v uživatelském dialogovém okně prezentováno za běhu uživatelům v jejich preferovaném jazyce.

### <a name="format-component"></a>Komponenta formátu

Když konfigurujete formát ER, můžete pro něj přidat označení ER. Atributy **Štítek** a **Text nápovědy** každého konfigurovaného zdroje dat lze propojit s označením ER, které je přidáno do formátu ER. Atributy **Štítek** a **Popis** každé hodnoty <a id="LinkFormatEnum"></a>výčtu formátu mohou být také spojeny se značkou ER, která je přístupná z upravitelného formátu ER.

> [!NOTE]
> Tyto atributy můžete také propojit s označením ER nadřazeného datového modelu ER, který znovu použije popisky modelu ve všech formátech ER nakonfigurovaných pro tento datový model ER.

Když je formát ER nakonfigurován tímto způsobem, obsah formátu bude představen uživatelům návrháře operací ER v preferovaném jazyce každého uživatele. Údržba formátu a analýza konfigurované logiky jsou proto zjednodušeny.

Protože formát ER je založen na datovém modelu ER, popisky na které se odkazuje v prvcích datového modelu, se objevují v návrháři formátu ER preferovaném jazyce uživatele.

Když je atribut **Štítek** datového zdroje **Vstupní parametr uživatele** nakonfigurován tak, že je spojen se štítkem ER, pole, které odpovídá parametru v uživatelském dialogovém okně za běhu, je poskytnuto uživatelům jako výzva. Následující obrázky ukazují, jak můžete propojit atribut **Štítek** datového zdroje **Vstupní parametr uživatele** v době návrhu na označení ER, takže uživatelé budou za běhu vyzváni k zadání parametru v různých uživatelsky upřednostňovaných jazycích (zobrazených pro angličtinu v USA (EN-US) a DE-AT).

![Zajištění překladu atributů vstupního parametru uživatele v návrháři operace ER](./media/er-multilingual-labels-refer-format.png)

![Zpracování plateb dodavatele ER za běhu pro uživatelsky preferovaný jazyk EN-US](./media/er-multilingual-labels-show-runtime-en.png)

![Zpracování plateb dodavatele ER za běhu pro uživatelsky preferovaný jazyk DE-AT](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Výrazy

Chcete-li použít štítek ve [výrazu](er-formula-language.md) ER, musíte použít syntaxi **@"GER\_LABEL:X"**, kde předpona **@** označuje, že operand odkazuje na štítek, **GER \_LABEL** označuje, že se jedná o štítek ER a **X** je ID štítku ER.

![Konfigurace výrazu ER obsahující odkaz na štítek ER v návrháři vzorců ER](./media/er-multilingual-labels-expression1.png)

Chcete-li odkazovat na systémový (aplikační) štítek, použijte syntaxi **@"X"**, kde předpona **@** označuje, že operand odkazuje na štítek a **X** je ID systémového štítku.

![Konfigurace výrazu ER obsahující odkaz na štítek aplikace v návrháři vzorců ER](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Mapování modelu

Výraz mapování modelu ER lze nakonfigurovat pomocí štítku. Když je toto mapování vyvoláno formátem ER, který je spuštěn za účelem generování odchozího dokumentu, zahrnuje kontext provádění kód jazyka. Konfigurovaný výraz výrazu bude vyplněn textem štítku, který byl nakonfigurován pro jazyk daného kontextu.

Pokud odkazovaný štítek nemá překlad pro jazyk kontextu provádění formátu, který volá mapování modelu, použije se místo toho text štítku v jazyce EN-US.

#### <a name="format"></a>Formát

Výraz ER mapování formátu ER lze nakonfigurovat pomocí štítků. Když je tento formát spuštěn spuštěn za účelem generování odchozího dokumentu, zahrnuje kontext provádění kód jazyka. Konfigurovaný výraz výrazu bude vyplněn textem štítku, který byl nakonfigurován pro jazyk daného kontextu.

![Poskytnutí překladu značky ER upravitelného výrazu ER v návrháři vzorců ER](./media/er-multilingual-labels-refer-in-expression.png)

![Ukázka vazby dat, která odkazuje na označení ER v návrháři operace ER](./media/er-multilingual-labels-refer-in-binding.png)

Můžete nakonfigurovat komponentu **FILE** formátu ER k vygenerování zprávy v preferovaném jazyce uživatele.

![Nastavte komponentu FILE v návrháři operací ER tak, aby se generovala zpráva v preferovaném jazyce uživatele](./media/er-multilingual-labels-language-context-user.png)

Pokud takto nakonfigurujete formát ER, sestava se vygeneruje pomocí odpovídajícího textu štítků ER. Následující obrázky ukazují příklady zpráv pro uživatelské jazyky EN-US a DE-AT.

![Náhled zprávy, která byla vygenerována v preferovaném jazyce uživatele US-US](./media/er-multilingual-labels-report-preview-en.png)

![Náhled zprávy, která byla vygenerována v preferovaném jazyce uživatele DE-AT](./media/er-multilingual-labels-report-preview-de.png)

Pokud odkazovaný štítek nemá překlad pro jazyk kontextu provádění formátu, použije se místo toho text štítku v jazyce EN-US.

## <a name="language"></a>Jazyk

ER podporuje různé způsoby, jak určit jazyk generované sestavy. V POLI **Jazykové preference** na kartě **Formát** můžete vybrat následující hodnoty:

- **Preference společnosti** - Vygenerujte sestavu ve firemním jazyce.

    ![V návrháři operací ER zadejte upřednostňovaný jazyk společnosti jako jazyk generované zprávy](./media/er-multilingual-labels-language-context-company.png)

- **Uživatelské preference** - Vygenerujte zprávu v preferovaném jazyce uživatele.
- **Explicitně definováno** - Generujte sestavu v jazyce, který je určen v době návrhu.

    ![V návrháři operací ER zadejte jazyk definovaný v době návrhu jako jazyk generované zprávy](./media/er-multilingual-labels-language-context-fixed.png)

- **Definováno při spuštění** - Generujte sestavu v jazyce, který je určen při spuštění. Pokud vyberete tuto hodnotu, v poli **Jazyk** nakonfigurujte výraz ER, který vrací kód jazyka pro daný jazyk, například jazyk příslušného zákazníka.

    ![V návrháři operací ER zadejte jazyk definovaný při spuštění jako jazyk generované zprávy](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a>Převod

Můžete přidat požadované štítky ER do upravitelné komponenty ER. Když je přidán štítek ER, může být přeložen dvěma způsoby: ručně a automaticky.

### <a name="manual-translation"></a>Ruční překlad

Když přidáte označení ER v **Překlad textu** [podokně](#TextTranslationPane), můžete jej ručně přeložit do všech jazyků, které jsou podporovány v aktuální instanci Finance. Upřednostňovaný jazyk můžete vybrat v poli **Jazyk** v sekci **Systémový jazyk** nebo **Jazyk uživatele**, zadejte příslušný text do příslušného pole **Přeložený text** a poté vyberte **Přeložit**. Tento proces musí být opakován pro každý požadovaný jazyk a pro každý štítek, který přidáte.

### <a name="automatic-translation"></a>Automatický překlad

Konfigurace komponenty ER se provádí v pracovní verzi konfigurace ER, v níž je upravitelná komponenta ER umístěna.

![Stránka ER Konfigurace nabízející přístup k verzi konfigurace ve stavu Koncept](./media/er-multilingual-labels-configurations.png)

Jak bylo popsáno výše v tomto tématu, můžete do upravitelné komponenty ER přidat požadované štítky ER. Tímto způsobem můžete určit text štítků ER v jazyce EN-US. Pak můžete exportovat štítky komponenty ER pomocí vestavěné funkce ER. Vyberte pracovní verzi konfigurace ER, která obsahuje upravitelnou součást ER, a poté vyberte **Směnka \> Export štítků**.

![Stránka Konfigurace ER umožňující exportovat štítky ER z vybrané verze pro potvrzení](./media/er-multilingual-labels-export.png)

Můžete exportovat všechny štítky nebo štítky pro jeden jazyk, který zadáte na začátku exportu. Štítky jsou exportovány jako soubor ZIP, který obsahuje soubory XML. Každý soubor XML obsahuje štítky pro jeden jazyk.

![Ukázka exportovaného souboru obsahujícího ER štítky pro jazyk DE-AT](./media/er-multilingual-labels-in-xml.png)

Tento formát se používá pro automatický překlad štítků externími překladatelskými službami, jako je [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md). Když obdržíte přeložené štítky, můžete je importovat zpět do pracovní verze konfigurace ER, která obsahuje komponenty ER, které tyto štítky vlastní. Vyberte pracovní verzi konfigurace ER, která obsahuje upravitelnou součást ER, a poté vyberte **Směnka \> Načíst štítky**.

![Stránka Konfigurace ER umožňující importovat štítky ER do vybrané verze konfigurace](./media/er-multilingual-labels-load.png)

Přeložené štítky budou importovány do vybrané konfigurace ER. Přeložené štítky, které existují v této konfiguraci ER, jsou nahrazeny. Pokud v konfiguraci ER chybí jakýkoli přeložený štítek, připojí se.

## <a name="lifecycle"></a>Životní cyklus

Štítky komponenty ER, které lze upravit, jsou spolu s dalším obsahem komponenty uloženy v příslušné verzi konfigurace ER.

Na popisy základní komponenty ER lze odkazovat v odvozené verzi komponenty ER, kterou vytvoříte, aby se zavedly vaše modifikace.

Verze verzí ER řídí přiřazení štítku k libovolnému atributu v komponentě ER. Změny přiřazení štítků jsou zaznamenány v seznamu změn (delta) editovatelné komponenty ER, která byla vytvořena jako odvozená verze poskytované komponenty ER. Tyto změny budou ověřeny, jakmile bude odvozená verze znovu převedena na novou základní verzi.

## <a name="functions"></a>Funkce

Vestavěná funkce ER [LISTOFFIELDS](er-functions-list-listoffields.md) umožňuje přístup k štítkům ER, které byly nakonfigurovány pro některé položky součástí ER.

Jak je popsáno výše v tomto tématu, atributy **Štítek** a **Popis** každé hodnoty výčtu ER [modelu](#LinkModelEnum) nebo [formátu](#LinkFormatEnum) může být spojena se štítkem ER, který je přístupný v příslušné komponentě ER. Můžete nakonfigurovat výraz ER, kde voláte funkci **LISTOFFIELDS** pomocí výčtu ER jako argumentu. Tento výraz vrací seznam, který obsahuje záznam pro každou hodnotu výčtu ER, který byl definován jako argument této funkce. Každý záznam obsahuje hodnotu štítku ER, který je spojen s hodnotou výčtu ER:

- Hodnota štítku ER, který je spojen s atributy **Štítek** je uložena v poli **Štítek** vráceného záznamu.
- Hodnota štítku ER, který je spojen s atributy **Popis** je uložena v poli **Popis** vráceného záznamu.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Funkce elektronického výkaznictví](er-formula-language.md#functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]