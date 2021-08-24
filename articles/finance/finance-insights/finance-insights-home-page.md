---
title: Domovská stránka Finanční přehledy (náhled)
description: Finanční přehledy poskytují konfigurovatelné a rozšiřitelné modely, které vám pomohou přesně a inteligentně předpovědět peněžní tok vaší společnosti, předpovědět, kdy obdržíte platbu za nevyrovnané pohledávky, a vygenerovat návrh rozpočtu, který může urychlit váš proces rozpočtování. Všechny tyto funkce jsou založeny na inteligentních modelech strojového učení.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8c9d5b9857e978eb5e591f4d854d687f33b438025e81fe2c827ab7ecdb2be4e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768812"
---
# <a name="finance-insights-home-page-preview"></a>Domovská stránka Finanční přehledy (náhled)

[!include [banner](../includes/banner.md)]

Finanční přehledy poskytují konfigurovatelné a rozšiřitelné modely, které vám pomohou přesně a inteligentně předpovědět peněžní tok vaší společnosti, předpovědět, kdy obdržíte platbu za nevyrovnané pohledávky, a vygenerovat návrh rozpočtu, který může urychlit váš proces rozpočtování. Všechny tyto funkce jsou založeny na inteligentních modelech strojového učení. Když jsou tyto nové funkce kombinovány s automatizací plateb a inkas od dodavatelů, poskytují bohatý a inteligentní finanční systém, který řídí rozhodování a pomáhá vám podniknout kroky k efektivní reakci na aktuální a očekávané obchodní výzvy.

> [!NOTE]
> Preview finančních přehledů je k dispozici pro nasazení v USA, Kanadě, Spojeném království, Evropě, Asii a Tichomoří, Austrálii a Novém Zélandu. Microsoft postupně přidává podporu pro další regiony. Chcete-li povolit Finance Insights na produkčním prostředí, je třeba nejprve aktivovat funkce [Export do Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) v produkčním prostředí.

> [!NOTE]
> Tato funkce je nabízena jako sada funkcí náhledu. Jako funkci náhledu byste neměli používat výsledné modely strojového učení k řízení nebo ovlivňování vašich obchodních rozhodnutí nebo návrhů rozpočtu. Vaše používání této funkce se řídí [Doplňkovými podmínkami použití](https://go.microsoft.com/fwlink/?linkid=2105274).

## <a name="prerequisites"></a>Předpoklady

V této části jsou uvedeny požadavky na používání Finančních přehledů. Kdekoli je to možné, jsou poskytovány odkazy na zdroje dalších informací.

### <a name="legal-requirements"></a>Právní požadavky

Chcete-li požádat o program náhledu, vyplňte [Náhled finančních přehledů pro smlouvu Dynamics 365 Finance](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Systémové požadavky

Pro zobrazení náhledu Finančních přehledů je vyžadováno prostředí úrovně 2 (multi-box). Základní informace o prostředích naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Požadavky verzí

Tento dokument se vztahuje na verzi 10.0.11 aplikace Finance and Operations (aktualizace platformy 35) a novější verze.

### <a name="historical-data-requirements"></a>Požadavky na historické údaje

K správnému trénování modelu strojového učení, který se používá pro funkci předpovědi plateb zákazníka, je zapotřebí alespoň jeden rok faktur zákazníka.

### <a name="role-and-permission-requirements"></a>Role a požadavky na povolení

Budou provedeny změny Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps a Azure. V těchto prostředích jsou vyžadována správná oprávnění. Zde jsou uvedeny některé příklady změn, které budou provedeny:

- Bude vytvořeno nové prostředí v Microsoft Power Platform.
- Účet úložiště, trezor klíčů a aplikace se vytvoří v Azure.
- Správce klienta Active Directory bude muset autorizovat aplikaci AI Builder pro přístup k datovému jezeru.
- Tato funkce bude zapnuta v Dynamics 365.

Znalost procesu vytváření a správy prostředků v Azure, Microsoft Dataverse a LCS vám budou nápomocny při dokončení tohoto procesu.

## <a name="configure-finance-insights"></a>Nakonfigurujte Finanční přehledy

Než budete moci používat Finanční přehledy, musíte dokončit některé konfigurační kroky. Další informace o postupu konfigurace Finance Insights najdete v:
  - Pro verze do 10.0.19: [Konfigurace pro Finance Insights (Preview) – verze až 10.0.19](configure-for-fin-insites.md).
  - Pro verze 10.0.20 a vyšší: [Konfigurace pro Finance Insights (náhled) - verze 10.0.20 a vyšší](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Vytvořte projekt integrátora dat

Budete muset vytvořit projekt integrátoru dat, aby do něj mohla proudit data, která generuje model strojového učení Dynamics 365 Finance. Kroky k vytvoření tohoto projektu najdete v části [Vytvořte projekt integrátoru dat](create-data-integrate-project.md).

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

Inteligentní předpovídání peněžních toků je postaveno na existující funkčnosti předpovídání peněžních toků v Dynamics 365 Finance. Chcete-li zkontrolovat stávající možnosti, přečtěte si [Prognózu peněžních toků](../cash-bank-management/cash-flow-forecasting.md).

- Pokud se chcete dozvědět, jak předpovědi plateb od zákazníka mohou poskytnout informace potřebné k proaktivnímu shromažďování, přečtěte si téma [Použijte předpovědi plateb zákazníka](use-customer-payment-predictions.md).
- Informace, které vám pomohou vyhodnotit účinnost predikčního modelu po zahájení používání této funkce, najdete v tématu [Vyhodnoťte model predikce počátečních plateb zákazníka](evaluate-payment-prediction.md).
- Informace, které vám mohou pomoci upravit data, která se používají k sestavení predikce, a tím zlepšit její účinnost, najdete v části [Vylepšete predikční model](improve-model.md).

Informace o výsledcích predikčních modelů AI naleznete ve [Výsledcích modelů strojového učení](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Použití prognóz cashflow

Možnost předpovědi peněžních toků vám pomůže přesněji odhadnout vaši peněžní pozici. 

- Informace o nových funkcích v předpovědích peněžních toků najdete v části [Předpověď peněžních toků](cash-flow-forecast-intro.md).
- Informace o importu externích dat, která chcete zahrnout do prognózy peněžních toků, naleznete v tématu [V předpovědích peněžních toků použijte externí data](external-data-in-cash-flow.md). 
- Informace o tom, jak použít model AI k promítnutí krátkodobých peněžních toků, najdete v části [Peněžní pozice](cash-position.md).
- Informace o ukládání pozic peněžních toků a předpovědi peněžních toků jako snímků a porovnání snímku se skutečnými najdete v části [Přehled snímků](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Pomocí návrhu rozpočtu

Informace o urychlení tvorby rozpočtu viz [Návrhy rozpočtu](budget-proposals.md). 

## <a name="feedback-and-support"></a>Zpětná vazba a podpora

Zašlete prosím e-mail na [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com), pokud máte zájem o poskytnutí názoru nebo potřebujete podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
