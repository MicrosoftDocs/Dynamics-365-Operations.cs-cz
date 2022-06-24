---
title: Nastavení experimentu
description: Tento článek popisuje, jak nastavit experiment ve službě třetí strany.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946159"
---
# <a name="set-up-an-experiment"></a>Nastavení experimentu

Jakmile [definujete hypotézu a určíte, jakou metriku úspěšnosti chcete používat](experimentation-identify.md), budete svůj experiment muset nastavit ve službě třetí strany. Následující schéma znázorňuje všechny kroky, které zahrnuje nastavení a spuštění experimentu na webu elektronického obchodu v Dynamics 365 Commerce. Další kroky jsou popsány v samostatných článcích.

[ ![Cesta uživatele experimentováním – nastavení.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Nastavení experimentu ve službě třetí strany
Nyní už byste měli mít vybranou službu třetí strany, abyste mohli spustit a monitorovat svůj experiment a nastavit konektor experimentování. Tyto předpoklady jsou uvedeny v tématu [Experimentování v Dynamics 365 Commerce](experimentation-overview.md).

Postupujte podle pokynů vyžadovaných k vytvoření experimentu ve službě třetí strany. Pokud je konektor správně nakonfigurován, objeví se kompletní seznam experimentů, které nastavíte ve službě třetí strany, v konfigurátoru webů Commerce asi do 5 minut.

## <a name="set-up-your-success-metrics"></a>Nastavení metriky úspěšnosti
Každý experiment potřebuje metriku k měření dopadu variant a k ověření hypotézy. Postupem podle pokynů níže povolte výpočet metriky ve službě třetí strany pomocí událostí živé telemetrie z Dynamics 365 Commerce.

Chcete-li nastavit metriky úspěchu pro moduly připravené k použití, postupujte takto.

1. V konfigurátoru webů Commerce vyberte kartu **Stránky** v levém navigačním podokně a pak vyberte stránku, pro kterou chcete metriku shromažďovat. 
1. Přejděte do části **Sledovaná ID událostí** v pravém podokně vlastností stránky nebo modulu, který chcete sledovat.
1. Vyberte **Zobrazit**. Zobrazí se seznam všech ID událostí kliknutí. Zkopírujte událost, kterou chcete sledovat, a vložte klíč této události do určeného umístění ve službě třetí strany. Pokud potřebujete více událostí, zkopírujte klíče postupně po jednom. 
1. Pro zobrazení stránky použijte SHA-256 hodnotu hash názvu stránky v nástroji pro tvorbu webu s připojeným `.PageView`. Například ID události pro `Homepage.PageView` by bylo `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Proveďte všechny další kroky pro sledování metriky vyžadované službou třetí strany.

V případě kliknutí na vlastní modul postupujte podle následujících kroků, abyste zpracovali události kliknutí:

1. Připravte objekt **TelemetryContent** pro modul pomocí funkce níže. Tato funkce bere jako vstupy název stránky, název modulu a výchozí objekt telemetrie poskytovaný sadou SDK.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Následuje příklad: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Vytvořte data datové části, která obsahují informace o tom, co je třeba zachytit. Pro tlačítka a další statické ovládací prvky můžete zahrnout **etext** například „Nakupovat“ nebo „Hledat“. A pro komponenty s kliknutím, jako je kliknutí na kartu produktu, můžete odeslat **recid**, což je ID záznamu produktu nebo ID produktu.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Jako příklad pro statické ovládací prvky předejte textový řetězec tlačítka, jak je znázorněno níže:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Jako příklad pro kliknutí na produkt předejte recordId produktu, jak je uvedeno níže:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Zavolejte funkci **OnClick** pro registraci události.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Následuje příklad:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Předchozí krok
[Identifikace hypotézy a určení metriky experimentu](experimentation-identify.md) 


## <a name="next-step"></a>Další krok
[Připojení a úpravy experimentu](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
