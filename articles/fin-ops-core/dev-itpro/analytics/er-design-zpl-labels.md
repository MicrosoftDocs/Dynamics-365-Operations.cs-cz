---
title: Návrh nového řešení ER pro tisk štítků ZPL
description: Toto téma vysvětluje, jak navrhnout nové řešení elektronického výkaznictví (ER) pro tisk štítků Zebra Programming Language (ZPL).
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: c1bedf1184b45741102000fa68c8d662c7383301
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612343"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Návrh nového řešení ER pro tisk štítků ZPL

[!include [banner](../includes/banner.md)]


Toto téma vysvětluje jak může uživatel v roli administrátora systému, vývojáře elektronických zpráv nebo funkčního konzultanta pro elektronické vykazování konfigurovat parametry rámce [elektronické vykazování (ER)](general-electronic-reporting.md), navrhovat požadované [konfigurace](general-electronic-reporting.md#Configuration) ER nového řešení ER pro přístup k datům systému Warehouse Management, a vygenerovat vlastní štítky lokality skladu ve formátu Zebra Programming Language (ZPL) II. Tyto kroky lze provést v rámci společnosti **USRT**.

## <a name="business-scenario"></a>Scénáře obchodu

Zastupujete společnost, která implementovala řízení skladu v Microsoft Dynamics 365 Finance. Každé skladové místo musí být označeno samolepicím štítkem, který obsahuje čárový kód. Pracovníci skladu budou ke skenování čárových kódů používat ruční čtečky čárových kódů.

Všechna skladová místa byla označena v rámci činností před uvedením do provozu. Musíte však mít také možnost tisknout štítky s umístěním skladu na vyžádání, pokud se stávající štítky poškodí nebo dojde k překonfigurování regálů ve skladu. Pomocí nedávno vydané funkce ER můžete nakonfigurovat nové řešení ER, které umožní vedoucímu skladu tisknout štítky přímo na termální tiskárně štítků.

## <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k návrhu nového řešení ER.

## <a name="design-a-domain-specific-data-model"></a>Návrh datového modelu specifického pro doménu

Vytvořte novou konfiguraci ER obsahující součást [datového modelu](er-overview-components.md#data-model-component) pro doménu Warehouse Management. Tento datový model bude později použit jako zdroj dat, když navrhujete formát ER pro generování štítků skladových míst.

### <a name="import-a-data-model-configuration"></a>Import konfigurace datového modelu

Chcete-li importovat požadovaný datový model ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků. Alternativně můžete vytvořit svůj vlastní datový model, jak je popsáno v další části.

1. Stáhněte si soubor [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Warehouse model.version.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

![Importovaná konfigurace datového modelu ER na stránce Konfigurace.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Vytvoření konfigurace datového modelu

Namísto importu souboru datového modelu od společnosti Microsoft můžete vytvořit datový model od začátku. Příklad, který ukazuje, jak dokončit tento úkol, viz [Vytvoření nové konfigurace datového modelu](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Kontrola datového modelu

Upravitelnou verzi nakonfigurovaného datového modelu můžete zobrazit na stránce **Návrhář datových modelů**.

![Struktura datového modelu ER na stránce Návrhář datového modelu.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Návrh mapování modelu pro konfigurovaný datový model

Jako uživatel v roli Electronic Reporting Developer musíte vytvořit novou konfiguraci ER, která obsahuje součást [mapování modelu](er-overview-components.md#model-mapping-component) pro datový model Skladu. Tato komponenta implementuje konfigurovaný datový model pro Dynamics 365 Finance a je specifická pro tuto aplikaci. Musíte ji nakonfigurovat, abyste určili aplikační objekty, které budou použity k vyplnění nakonfigurovaného datového modelu aplikačními daty za běhu. K provedení tohoto úkolu musíte chápat implementaci datové struktury obchodní domény Warehouse management ve Financích.

### <a name="import-a-model-mapping-configuration"></a>Import konfigurace mapového modelu

Chcete-li importovat požadované mapování modelu ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků. Alternativně můžete vytvořit vlastní mapování modelu, jak je popsáno v další části.

1. Stáhněte si soubor [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Warehouse model mapping.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

![Importovaná konfigurace mapování modelu ER na stránce Konfigurace.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Vytvoření konfigurace mapování modelu

Namísto importu souboru mapování modelu od společnosti Microsoft můžete vytvořit mapování modelu od začátku. Příklad, který ukazuje, jak dokončit tento úkol, viz [Vytvoření nové konfigurace mapování modelu](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Kontrola mapování modelu

Upravitelnou verzi nakonfigurovaného mapování modelu můžete zobrazit na stránce **Návrhář mapování modelu**.

![Struktura mapování modelu ER na stránce Návrhář mapování modelu.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Návrh formátu

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte vytvořit novou konfiguraci ER, která obsahuje komponent [formát](er-overview-components.md#format-component). Ke konfiguraci této komponenty použijete kód ZPL II k určení rozvržení štítku umístění vašeho skladu.

### <a name="import-a-format-configuration"></a>Importování konfigurace formátu

Chcete-li importovat požadovaný formát ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků. Alternativně můžete vytvořit svůj vlastní formát, jak je popsáno v další části.

1. Stáhněte si soubor [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Warehouse location labels.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

![Importovaná konfigurace formátu ER na stránce Konfigurace.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Vytvoření konfigurace formátu

Namísto importu souboru formátu od společnosti Microsoft můžete vytvořit formát od začátku. Příklad, který ukazuje, jak dokončit tento úkol, viz [Vytvoření nové konfigurace formátu](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Kontrola formátu

Upravitelnou verzi nakonfigurovaného formátu můžete zobrazit na stránce **Návrhář formátů**.

![Struktura formátu ER na stránce Návrhář formátů.](./media/er-design-zpl-labels-format.png)

Zdroj dat `model.Location.Label` tohoto formátu je nakonfigurován tak, aby generoval štítky, které obsahují následující informace:

- Název skladu jako text
- Název skladu jako čárový kód
- Název umístění
- Kontrolní číslice

Na stránce **Návrhář vzorce** pro zdroj dat obsahuje vzorec ER, který se používá ke generování štítků, funkci `CONCATENATE`, která kombinuje informace v požadovaném rozložení.

![Vzorec pro zdroj dat na stránce návrháře vzorců.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Rozvržení štítku je navrženo tak, aby název umístění a kontrolní číslice byly zarovnány do středu štítku. ZPL II však nepodporuje zarovnání na střed pro čárové kódy. Proto se vzorec zdroje dat `model.Location.Warehouse.Alignment` používá k zarovnání čárového kódu na střed štítku. Tento vzorec vypočítá levý posun čárového kódu na základě počtu znaků v názvu skladu.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Připravte své prostředí na náhled generovaných štítků

Následující příklad používá aplikaci emulátoru tiskárny pro štítky ZPL k zobrazení náhledu vygenerovaných štítků na obrazovce. K aktivaci této funkce postupujte následovně.

1. Přidejte cíl ER [Tiskárna](er-destination-type-print.md) pro formát ER **Štítek umístění skladu** a nakonfigurujte ho tak, aby odesílal vygenerované štítky z Finance do [Agent pro směrování dokumentů (DRA)](install-document-routing-agent.md).
2. Nainstalujte a nakonfigurujte DRA pro směrování generovaných štítků z Finance na místní tiskárnu, která je přístupná z aktuální pracovní stanice.
3. Přidejte místní tiskárnu pro aktuální pracovní stanici a nakonfigurujte ji tak, aby předávala vygenerované štítky z DRA do aplikace emulátoru tiskárny.
4. Nainstalujte si aplikaci emulátoru tiskárny jako rozšíření webového prohlížeče Chrome a nakonfigurujte ji tak, aby předávala vygenerované štítky z místní tiskárny webové službě, která vygenerované štítky vykreslí a vrátí je do emulátoru tiskárny k náhledu.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>Sestava ER</p>
<p>Cílové místo tiskárny</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Agent pro směrování dokumentů</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Místní tiskárna</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Emulátor tiskárny</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Vykreslovací webová služba</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Instalace a konfigurace aplikace emulátoru tiskárny

Přidejte si do webového prohlížeče Chrome aplikaci emulátoru tiskárny pro vykreslovací modul ZPL. Tento příklad používá emulátor [Zpl Printer](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo), který je založen na [webové službě Labelary ZPL](http://labelary.com/service.html). Aplikace emulátoru tiskárny předá vygenerované štítky ve formátu ZPL z místní tiskárny webové službě a poté vrátí štítky jako soubory PDF nebo PNG k náhledu.

1. V internetovém obchodě Chrome vyhledejte a vyberte aplikaci emulátoru tiskárny, kterou chcete použít. Poté vyberte **Přidat do Chromu** pro přidání do webového prohlížeče Chrome.

    ![Přidání aplikace emulátoru tiskárny do webového prohlížeče Chrome z internetového obchodu Chrome.](./media/er-design-zpl-labels-add-app.png)

2. Vyberte **Spustit aplikaci** ke spuštění aplikace emulátoru tiskárny z webového prohlížeče Chrome.

    ![Spuštění aplikace emulátoru tiskárny z webového prohlížeče Chrome.](./media/er-design-zpl-labels-run-app.png)

3. Nakonfigurujte spuštěnou aplikaci:

    1. Vypněte aplikaci.
    2. V nastavení tiskárny nastavte hostitele na **127.0.0.1**.
    3. Nastavte port na **9100**.

        ![Konfigurace aplikace emulátoru tiskárny.](./media/er-design-zpl-labels-configure-app.png)

    4. Aplikaci znovu zapněte. Měli byste obdržet zprávu, že tiskárna byla spuštěna na zadaném hostiteli a portu.

        ![Aplikace emulátoru tiskárny byla znovu zapnuta.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Protože aplikace emulátoru tiskárny, která je použita v tomto příkladu, využívá k vykreslování štítků webovou službu, ujistěte se, že vaše nastavení zabezpečení umožňuje komunikaci se službou. V opačném případě aplikace neobdrží vykreslené štítky a nebude k dispozici žádný náhled těchto štítků.

### <a name="add-and-configure-a-local-printer"></a>Přidání a konfigurace místní tiskárny

[Přidejte novou místní tiskárnu](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b), kterou může aktuální zařízení používat, aby předávala vygenerované štítky z DRA do aplikace emulátoru tiskárny.

1. V systému Windows vyberte **Start** \> **Nastavení** \> **Zařízení** \> **Tiskárny \& skenery**.
2. Vyberte **Nastavení tiskáren \& skenerů**.
3. V části **Přidat tiskárnu nebo skener** vyberte **Přidat zařízení**.
4. V části **Tiskárna, kterou chci, není uvedena** vyberte **Přidat ručně**.
5. V poli **Najít tiskárnu podle dalších možností** vyberte **Přidat místní tiskárnu nebo síťovou tiskárnu s ručním nastavením**.
6. V poli **Vybrat port tiskárny** vyberte **Vytvořit nový port** a poté postupujte takto:

    1. Do pole **Typ portu** vyberte **Standardní port TCP/IP**.
    2. Do pole **Název hostitele nebo IP adresa** zadejte **127.0.0.1**.
    3. Do pole **Název portu** zadejte **ZPL**.
    4. Počkejte, až dokončí operace **Detekce TCP/IP portu**.
    5. V poli **Typ zařízení** vyberte **Vlastní** a poté vyberte **Nastavení**.
    6. Ujistěte se, že jsou zadána následující nastavení portu:

        - **Název portu**: ZPL
        - **Název tiskárny nebo IP adresa:** 127.0.0.1
        - **Protokol:** Raw
        - **Číslo portu:** 9100

7. V poli **Nainstalovat ovladač tiskárny** vyberte **Obecný / pouze text**.
8. Do pole **Název tiskárny** zadejte **ZebraPrinter**.

![Přidání místní tiskárny pro aktuální zařízení.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Instalace a konfigurace DRA

Připravte DRA na předání vygenerovaných štítků z Finance do nakonfigurované místní tiskárny.

1. [Nainstalujte DRA](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Nakonfigurujte DRA](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Zaregistrujte místní tiskárnu](install-document-routing-agent.md#register-network-printers) v DRA.
4. [Aktivujte místní tiskárnu](install-document-routing-agent.md#administer-network-printers) v prostředí Finance.

![Příprava DRA k tisku generovaných štítků.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Konfigurujte cíle ER

Připravte cíl ER na předání vygenerovaných štítků z Finance do DRA.

1. Přejděte do nabídky **Správa organizace** \> **Elektronická sestava** \> **Místo určení elektronického výkaznictví**.
2. Na stránce **Cíl elektronického výkaznictví** v podokně akcí vyberte **Nový**.
3. V poli **Odkaz** vyberte **Štítky umístění skladu**.
4. Na záložce **Místo určení souboru** vyberte **Nové**.
5. Do pole **Název** zadejte **Štítky**.
6. V poli **Název součásti souboru** vyberte **Sestava**.
7. Vyberte **Nastavení**.
8. V dialogovém okně **Nastavení cíle** na kartě **Tiskárna** nastavte možnost **Povoleno** možnost na **Ano**.
9. Do pole **Název tiskárny** zadejte **ZebraPrinter**.
10. V poli **Typ směrování dokumentu** vyberte **ZPL**.
11. Vyberte **OK**.

![Konfigurace cíle ER pro formát štítků skladového místa na stránce Cíle elektronického hlášení.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Kontrola umístění ve skladu

1. Přejděte do nabídky **Warehouse management** \> **Nastavení** \> **Sklad** \> **Umístění**.
2. Na stránce **Umístění** filtrem zobrazíte pouze místa, která mají hodnotu v poli **Kontrolní číslice**.

![Kontrola umístění skladu na stránce Umístění.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Tisk štítků s umístěním skladu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurace rozbalte **Model skladu** a vyberte **Štítky skladových míst**.
3. V podokně akcí zvolte **Spustit**.
4. V dialogovém okně **Parametry elektronického výkaznictví** na kartě **Záznamy k zahrnutí** vyberte **Filtrovat**.
5. Na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Tabulka** nastavena na **Umístění** a pole **Pole** je nastaveno na **Umístění**. Do pole **Kritéria** zadejte **LPEnabled**.
6. Vyberte **OK**.
7. Vyberte **OK**. Vygeneruje se štítek a zobrazí se na stránce náhledu v aplikaci emulátoru tiskárny.

![Kontrola vygenerovaného štítku na stránce náhledu v aplikaci emulátoru tiskárny Zpl.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Úprava rozvržení štítku

Můžete změnit aktuální rozvržení štítků umístění skladu. Následující příklad ukazuje, jak změnit rozložení tak, aby vygenerované štítky obsahovaly ID profilu umístění.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Nastavte volbu [uživatelský parametr ER](electronic-reporting-destinations.md#applicability) **Použít cíle pro stav konceptu** na **Ano**.
3. Na stránce **Konfigurace** ve stromu konfigurace rozbalte **Model skladu** a vyberte **Štítky skladových míst**.
4. Vyberte možnost **Návrhář**.
5. Na stránce **Návrhář formátu** na kartě **Mapování** vybete zdroj dat `model.Location.Label`.
6. V dialogovém okně **Vlastnosti zdroje dat** vyberte **Upravit** \> **Upravit vzorec**.
7. Na stránce **Návrhář vzorců** v poli **Vzorec** zkontrolujte vzorec ER, který se používá ke generování štítků.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Aktualizujte vzorec a přidejte k vygenerovaným štítkům ID profilu umístění.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Zvolte možnost **Uložit**.
10. Vyberte **OK**.
11. V podokně akcí zvolte **Spustit**.
12. V dialogovém okně **Parametry elektronického výkaznictví** na kartě **Záznamy k zahrnutí** vyberte **Filtrovat**.
13. Na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Tabulka** nastavena na **Umístění** a pole **Pole** je nastaveno na **Umístění**. V poli **Kritéria** zadejte **Brána**.
14. Vyberte **OK**.
15. Vyberte **OK**. Vygeneruje se štítek a zobrazí se na stránce náhledu v aplikaci emulátoru tiskárny.

![Kontrola vygenerovaného štítku, který obsahuje ID profilu umístění na stránce náhledu aplikace emulátoru tiskárny Zpl.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kódování

> [!NOTE]
> Musíte synchronizovat nastavení kódování komponenty **Common\\File** editovatelného formátu ER a příslušné nastavení navrženého štítku. Hodnota pole **[Kódování](er-suppress-bom-characters.md)** komponenty **Common\\File** by neměla odporovat příkazu ZPL, který se používá k řízení kódování štítku (například příkaz `^CI`). ER neověřuje, že jsou tato nastavení synchronizována.

## <a name="additional-resources"></a>Další prostředky

[Cílové místo tiskárny](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
