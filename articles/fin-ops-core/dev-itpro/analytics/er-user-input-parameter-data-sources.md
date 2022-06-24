---
title: Pomocí zdrojů dat PARAMETR UŽIVATELSKÝ VSTUP zadejte parametry pro sestavu
description: Tento článek vysvětluje, jak používat zdroje dat PARAMETR VSTUPU UŽIVATELE ke specifikaci parametrů pro sestavy, které generujete.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872965"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Pomocí zdrojů dat PARAMETR UŽIVATELSKÝ VSTUP zadejte parametry pro sestavu

[!include[banner](../includes/banner.md)]

Když navrhujete komponenty [Elektronické hlášení](general-electronic-reporting.md) (ER), [mapování modelu](er-overview-components.md#model-mapping-component) a ER [formát](er-overview-components.md#format-component), můžete použít zdroje dat *PARAMETR VSTUPU UŽIVATELE*, abyste získali požadované hodnoty, které lze zadat v polích pro zadávání dat v dialogovém okně za běhu, před zahájením provádění formátu ER. Tento článek popisuje zdroje dat *PARAMETR VSTUPU UŽIVATELE*, které jsou aktuálně podporovány.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Povinné vlastnosti

Musíte zadat následující vlastnosti pro datový zdroj každého typu *PARAMETR VSTUPU UŽIVATELE*:

- V poli **Název** zadejte interní název zdroje dat. Tento název můžete použít v ostatních [výrazech](er-formula-language.md) a vazbách nakonfigurovaného mapování modelu nebo komponenty formátu.

## <a name="optional-properties"></a><a name="optional-properties"></a>Volitelné vlastnosti

Můžete také zadat následující vlastnosti pro datový zdroj typu *PARAMETR VSTUPU UŽIVATELE*:

- V polí **Popisek** zadejte popisek, který se používá pro související pole pro zadávání dat v dialogovém okně za běhu. Můžete přidat jiný text štítku pro různé kódy jazyků aktivací pole **Popisek** a poté výběrem **Přeložit**.
- V poli **Pomoc** zadejte text nápovědy, který se zobrazí v době návrhu v dolní části stránky **Návrhář formátů** nebo **Návrhář mapování modelů**, když je vybrán upravitelný zdroj dat typu *PARAMETR VSTUPU UŽIVATELE*. Tento text může poskytnout další podrobnosti o zdroji dat, které uživatelům pomohou při konfiguraci upravitelného formátu nebo komponenty mapování modelu. Můžete přidat různé texty nápovědy pro různé kódy jazyků výběrem **Přeložit**.

    > [!NOTE]
    > Tlačítko **Přeložit**, které můžete použít k přidání [štítků a textu specifických pro daný jazyk](er-design-multilingual-reports.md#format-component), se zpřístupní až poté, co přidáte zdroj dat, uložíte změny a poté zdroj dat znovu otevřete pro úpravy.

- V poli **Pouze ke čtení** nakonfigurujte výraz, který vrací *[logickou](er-formula-supported-data-types-primitive.md#boolean)* hodnotu.

    - Pokud nakonfigurovaný výraz vrátí hodnotu **True** za běhu, pole pro zadání souvisejících dat v dialogovém okně se zobrazí šedě a jeho hodnotu nelze změnit.
    - Pokud nakonfigurovaný výraz vrátí hodnotu **False** za běhu nebo pokud není konfigurovaný žádný výraz, pole pro zadání souvisejících dat je dostupné v dialogovém okně a jeho hodnotu lze změnit.

- V poli **Výchozí hodnota** nakonfigurujte výraz, který vrací hodnotu odkazovaného typu parametru. Tuto hodnotu lze použít k vyplnění výchozí hodnoty pro související pole zadávání dat v dialogovém okně za běhu.

    Když spustíte formát ER, hodnota, kterou zadáte do příslušného pole pro zadávání dat v dialogovém okně za běhu, se uloží do paměti jako dříve použitá hodnota. Dříve používané hodnoty se ukládají jednotlivě pro každé pole, běžící formát ER, aktuálního uživatele a aktuální organizaci (společnost).

    - Nastavte možnost **Vždy resetovat na výchozí hodnotu** na **Ano**, pokud by hodnota, která je vrácena výrazem **Výchozí hodnota** vždy měla být použita jako výchozí hodnota, bez ohledu na dříve použitou hodnotu.
    - Nastavte možnost **Vždy resetovat na výchozí hodnotu** na **Ne**, pokud by hodnota, která je vrácena výrazem **Výchozí hodnota** měla být použita jako výchozí hodnota pouze tehdy, když dříve použitá hodnota chybí.

    > [!NOTE]
    > Pokud nastavíte možnost **Vždy resetujte na výchozí hodnotu** na **Ano**, výraz musí být nakonfigurován v poli **Výchozí hodnota**.

- Pokud nastavíte možnost **Povolit vícenásobný výběr** na **Ano**, můžete za běhu vybrat více hodnot pro nakonfigurovaný parametr. Pokud ji nastavíte na **Ne**, můžete vybrat pouze jednu hodnotu.

    > [!NOTE]
    > Tato možnost neplatí pro všechny typy *PARAMETR VSTUPU UŽIVATELE*. V době návrhu je vyvolána výjimka, která informuje uživatele, že nakonfigurovaný vstupní parametr uživatele nepodporuje vícenásobný výběr a že lze vybrat nebo zadat pouze jednu hodnotu.
    >
    > Pokud nastavíte možnost **Povolit vícenásobný výběr** na **Ano** a zadali jste výraz v poli **Výchozí hodnota**, lze tento výraz použít k nastavení pouze jedné výchozí hodnoty.

- Vyberte možnost **Upravit viditelnost**, chcete-li určit, zda se má nakonfigurovaný parametr zobrazit v dialogovém okně za běhu.

    > [!NOTE]
    > Výchozí viditelnost zdrojů dat typu *PARAMETR VSTUPU UŽIVATELE* závisí na komponentě ER, která je drží.
    >
    > - Pokud je zdroj dat nakonfigurován v komponentě formátu, je ve výchozím nastavení viditelný.
    > - Pokud je zdroj dat nakonfigurován v komponentě mapování modelu, je viditelný pouze v případě, že hodnota zdroje dat ovlivní výsledek při spuštění komponenty ER. Například jste přidali zdroj dat, ale nepoužili jste jej ve výrazech a vazbách aktuální komponenty mapování modelu. V tomto případě se ve výchozím nastavení příslušné pole pro zadání dat v dialogovém okně za běhu nezobrazí. 

    Na stránce **Návrhář receptury** v poli **Receptura** nakonfigurujte výraz, který vrací *logickou* hodnotu.

    - Pokud nakonfigurovaný výraz vrátí hodnotu **True** za běhu nebo pokud není konfigurovaný žádný výraz, pole pro zadání souvisejících dat je viditelné v dialogovém okně za běhu.
    - Pokud nakonfigurovaný výraz vrátí hodnotu **False**, související pole pro zadávání dat je za běhu skryto v dialogovém okně. Když je za běhu volána jinými výrazy, vrátí výchozí hodnotu, dříve použitou hodnotu nebo výchozí hodnotu pro aktuální hodnotu datového typu v závislosti na dalších nastaveních.

## <a name="type-specific-properties"></a>Typově specifické vlastnosti

### <a name="application-dependent-user-input-parameter"></a>Vstupní parametr uživatele závislý na aplikaci

Použijte zdroj dat **Všeobecné** \> **Vstupní parametr uživatele** k získání požadované hodnoty nebo hodnot datového typu, který je zadán pro aktuální instanci aplikace Microsoft Dynamics 365 Finance. Když přidáte zdroj dat tohoto typu do komponenty ER, zadejte následující vlastnosti:

- V poli **Název datového typu operací (EDT, enum)** vyberte [rozšířený datový typ (EDT)](../extensibility/extensible-edts.md) aplikace nebo výčet aplikací.

> [!NOTE]
> Doporučujeme, abyste si prohlédli výrazy, které jsou nakonfigurovány v polích **Pouze ke čtení** a **Výchozí hodnota**, když změníte odkaz **Název datového typu operací (EDT, enum)** v upravitelném zdroji dat tohoto typu *PARAMETR VSTUPU UŽIVATELE*.

Následující obrázek ukazuje vlastnosti datového zdroje `$TaxRegNum`, který byl nakonfigurován v konfiguraci formátu ER **Instat XML (DE)**. Tento zdroj dat je nakonfigurován pro použití EDT *Popis* k nabídnutí typu dat **Daňové registrační číslo** pro zadávání dat v dialogovém okně za běhu.

![Vlastnosti zdroje dat PARAMETR VSTUPU UŽIVATELE zadejte do dialogového okna na stránce Návrhář formátů.](./media/er-user-input-parameter-data-sources-01.png)

Následující obrázek ukazuje dialogové okno, které se zobrazí za běhu, když je konfigurace formátu ER **Instat XML (DE)** je spuštěna ke [generování](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) výkazu pro Intrastat. Všimněte si, že nakonfigurované pole **Daňové registrační číslo** je k dispozici pro zadávání dat.

![Dialogové okno Zpráva Intrastat spuštěného formátu ER na stránce Intrastat.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Vstupní parametr uživatele () pro výčet datového modelu

Použijte zdroj dat typu **Datový model** \> **Vstupní parametr uživatele výčtu**, abyste získali požadovanou hodnotu nebo hodnoty jednoho datového modelu [výčet](er-formula-supported-data-types-primitive.md#enumeration). Když přidáte zdroj dat tohoto typu do komponenty ER, zadejte následující vlastnosti:

- Do pole **Model** zadejte odkaz na základní datový model.
- Do pole **Výčet modelů** zadejte odkaz na výčet odkazovaného datového modelu.
- V poli **Verze** vyberte číslo revize komponenty datového modelu ER, která obsahuje výčet odkazovaného modelu.

    > [!TIP]
    > V době návrhu můžete nechat pole **Verze** prázdné pro přístup k seznamu výčtů pro odkazovanou komponentu datového modelu, která se nachází v pracovní verzi odpovídající konfigurace datového modelu ER. Tímto způsobem můžete současně upravovat verzi konceptu komponenty mapování modelu nebo formátu a verzi konceptu komponenty základního datového modelu.
    >
    > Všimněte si však, že pole **Verze** lze ponechat prázdné pouze ve verzi konceptu mapování modelu nebo komponenty formátu. Když změníte stav mapování modelu ER nebo konfiguraci formátu z **Koncept** na **Dokončeno**, je toto pole automaticky vyplněno nejvyšším číslem revize modelu, které je k dispozici v aktuální instanci Finance. Pokud zavedete nový výčet nebo novou hodnotu výčtu do pracovní verze svého základního datového modelu a odkazujete na něj v upravitelném mapování modelu nebo komponentě formátu, dokončete tuto pracovní verzi konfigurace základního datového modelu před tím, než je dokončen koncept verze vašeho ER, mapování modelu nebo konfigurace formátu. V opačném případě bude vyvolána výjimka „Cesta nenalezena“, když změníte stav mapování modelu nebo konfiguraci formátu z **Koncept** na **Dokončeno**. Zpráva vás bude informovat, že v základním datovém modelu chybí odkazovaný výčet nebo hodnota výčtu.

Následující obrázek ukazuje vlastnosti datového zdroje `$ReportDirection`, který byl nakonfigurován v konfiguraci formátu ER **Instat XML (DE) Contoso**. Konfigurace **Instat XML (DE) Contoso** byla [odvozena](general-electronic-reporting.md#Configuration) z konfigurace **Instat XML (DE)**. Tento zdroj dat je nakonfigurován pro použití výčtu modelů *ReportDirection* k nabídnutí vhodného vyhledávacího pole v dialogovém okně za běhu.

![Vlastnosti zdroje dat PARAMETR VSTUPU UŽIVATELE zadejte do dialogového okna na stránce Návrhář formátů.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Vstupní parametr uživatele výčtu formátu

Použijte zdroj dat typu **Výšet formátů** \> **Vstupní parametr uživatele výčtu**, abyste získali požadovanou hodnotu nebo hodnoty jednoho výčtu formátů. Když přidáte zdroj dat tohoto typu do komponenty ER, zadejte následující vlastnosti:

- Do pole **Formát výčtu** zadejte výčet upravitelných formátů.

> [!NOTE]
> Datové zdroje tohoto typu lze konfigurovat pouze v rozsahu komponenty upravitelného formátu.

## <a name="additional-resources"></a>Další prostředky

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Inicializace hodnot zdroje dat typu USER INPUT PARAMETER ze zdrojového kódu](er-initiate-uip-data-source-value-from-source-code.md)
