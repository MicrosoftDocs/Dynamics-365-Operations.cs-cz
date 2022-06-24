---
title: Domovská stránka Finance Insights
description: Finanční přehledy poskytují konfigurovatelné a rozšiřitelné modely, které vám pomohou přesně a inteligentně předpovědět peněžní tok vaší společnosti, předpovědět, kdy obdržíte platbu za nevyrovnané pohledávky, a vygenerovat návrh rozpočtu, který může urychlit váš proces rozpočtování. Všechny tyto funkce jsou založeny na inteligentních modelech strojového učení.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 42ea8884c357bcb26ac96df8dca75e7ff449d4f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881955"
---
# <a name="finance-insights-home-page"></a>Domovská stránka Finance Insights

[!include [banner](../includes/banner.md)]

Finance Insights poskytují konfigurovatelná a rozšiřitelná řešení, která vám pomohou inteligentně předpovědět peněžní tok vaší společnosti, předpovědět, kdy obdržíte platbu za nevyrovnané pohledávky, a vygenerovat návrh rozpočtu, který pomůže urychlit váš proces rozpočtování. Tyto funkce využívají inteligentní šablony strojového učení k vytváření modelů pomocí dat, která poskytnete (včetně dat od třetí strany, jako jsou informace o spotřebitelských zprávách ze střediska). Tyto inteligentní schopnosti informují o rozhodování a pomáhají vám podnikat kroky k efektivní reakci na aktuální a očekávané obchodní výzvy. Jste odpovědní za jakákoli data, která se používají s Finance Insights nebo z nich vychází.

> [!NOTE]
> Finance Insights je k dispozici pro nasazení v USA, Kanadě, Spojeném království, Evropě, Asii a Tichomoří, Japonsku, Austrálii a Novém Zélandu. Microsoft postupně přidává podporu pro další regiony.

## <a name="prerequisites"></a>Předpoklady

V této části jsou uvedeny požadavky na používání Finančních přehledů. Kdekoli je to možné, jsou poskytovány odkazy na zdroje dalších informací.

### <a name="system-requirements"></a>Systémové požadavky

Pro zobrazení náhledu Finančních přehledů je vyžadováno prostředí úrovně 2 (multi-box). Základní informace o prostředích naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Požadavky verzí

Tento článek se týká Microsoft Dynamics 365 Finance verze 10.0.21 a novější.

### <a name="license-requirements"></a>Požadavky na licence

Finance Insights využívá kredity AI Builder pro vytváření finančních předpovědí. Všechny potřebné licence k tomu jsou součástí licence tenanta. Každý klient Dynamics 365 Finance má 20 000 kreditů AI Builder každý měsíc. Pokud jsou pro obchodní potřeby vyžadovány další kredity, lze je zakoupit přímo od AI Builder.

### <a name="historical-data-requirements"></a>Požadavky na historické údaje

K správnému trénování modelu strojového učení, který se používá pro funkci předpovědi plateb zákazníka, je zapotřebí alespoň jeden rok faktur zákazníka. Pro prognózy peněžních toků se doporučují tři roky historických dat. Pro inteligentní návrhy rozpočtu se doporučují tři roky historického rozpočtu a/nebo skutečnosti.

## <a name="configure-finance-insights"></a>Konfigurace Finance insights

Než budete moci používat Finance Insights, musíte dokončit některé konfigurační kroky. Pro další informace o tom, jak konfigurovat Finanční přehledy, viz [Konfigurace pro Finanční přehledy](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Vytvořte projekt integrátora dat

Budete muset vytvořit projekt integrátoru dat, aby do Dynamics 365 Finance mohla proudit data, která generuje model strojového učení. Kroky k vytvoření tohoto projektu najdete v části [Vytvořte projekt integrátoru dat](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Povolit funkce Finanční přehledy

Po dokončení konfiguračních kroků a nastavení demo dat musíte zapnout a nastavit všechny funkce, které plánujete použít: předpovědi plateb zákazníků, prognózy peněžních toků a návrhy rozpočtu.

### <a name="enable-customer-payment-predictions"></a>Povolit předpovědi plateb od zákazníka
Pokud používáte demo data k testování předpovědí plateb zákazníků, možná budete muset importovat další demo data, abyste mohli úspěšně vytvořit svůj model AI. 

Chcete-li povolit předpovědi plateb od zákazníka, musíte dokončit sadu kroků k vytvoření modelu strojového učení, který využívá data vaší organizace k vygenerování předpovědí o tom, kdy zákazníci pravděpodobně zaplatí neuhrazené faktury a kdy budou pravděpodobně zaplaceny konkrétní faktury. Další informace a konkrétní kroky k dokončení najdete v části [Povolit předpovědi plateb od zákazníka](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Povolit prognózu cashflow
Chcete-li povolit předpovídání peněžních toků, musíte dokončit sadu kroků k vytvoření modelu strojového učení, který využívá údaje vaší organizace k vygenerování předpovědí peněžních toků. Další informace a konkrétní kroky k dokončení najdete v části [Povolit předpovědi cashflow](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Povolit návrhy rozpočtu

Funkce Rozpočtové návrhy používá k vygenerování návrhu rozpočtu model strojového učení spolu s historickými daty vaší organizace. Vygenerovaný návrh vám pomůže zahájit proces rozpočtování, který je efektivnější než manuální proces. Konkrétní kroky k povolení této funkce najdete v části [Povolit návrhy rozpočtu](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Používání funkcí Finančních přehledů

### <a name="using-customer-payment-predictions"></a>Používání předpovědí plateb od zákazníka

- Pokud se chcete dozvědět, jak předpovědi plateb od zákazníka mohou poskytnout informace potřebné k proaktivnímu začátku shromažďování, přečtěte si téma [Použijte předpovědi plateb zákazníka](use-customer-payment-predictions.md).
- Informace, které vám pomohou vyhodnotit účinnost predikčního modelu po zahájení používání této funkce, najdete v tématu [Vyhodnoťte model predikce počátečních plateb zákazníka](evaluate-payment-prediction.md).
- Informace, které vám mohou pomoci upravit data, která se používají k sestavení predikce, a tím zlepšit její účinnost, najdete v části [Vylepšete predikční model](improve-model.md).
- Informace o výsledcích predikčních modelů AI naleznete ve [Výsledcích modelů strojového učení](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Použití prognóz cashflow

Možnost předpovědi peněžních toků vám pomůže přesněji odhadnout vaši peněžní pozici. Inteligentní předpovídání peněžních toků je postaveno na existující funkčnosti předpovídání peněžních toků v Dynamics 365 Finance. Chcete-li zkontrolovat stávající možnosti, přečtěte si [Prognózu peněžních toků](../cash-bank-management/cash-flow-forecasting.md).

- Informace o nových funkcích v předpovědích peněžních toků najdete v části [Předpověď peněžních toků](cash-flow-forecast-intro.md).
- Informace o importu externích dat, která chcete zahrnout do prognózy peněžních toků, naleznete v tématu [V předpovědích peněžních toků použijte externí data](external-data-in-cash-flow.md). 
- Informace o tom, jak použít model AI k promítnutí krátkodobých peněžních toků, najdete v části [Peněžní pozice](cash-position.md).
- Informace o ukládání pozic peněžních toků a předpovědi peněžních toků jako snímků a porovnání snímku se skutečnými najdete v části [Přehled snímků](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Pomocí návrhu rozpočtu

Informace o urychlení tvorby rozpočtu viz [Návrhy rozpočtu](budget-proposals.md). 

## <a name="feedback-and-support"></a>Zpětná vazba a podpora

Pokud máte zájem o poskytnutí zpětné vazby nebo pokud vyžadujete technickou podporu, zašlete prosím e-mail na [Finance Insights](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
