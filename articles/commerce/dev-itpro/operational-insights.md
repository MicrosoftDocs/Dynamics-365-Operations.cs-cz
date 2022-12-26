---
title: Nastavení Operational Insights
description: Tento článek popisuje, jak nastavit a používat funkci Operational Insights v Microsoft Dynamics 365 Commerce.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832117"
---
# <a name="set-up-operational-insights"></a>Nastavení Operational Insights

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nastavit a používat funkci Operational Insights v Microsoft Dynamics 365 Commerce.

Operational Insights je funkce Dynamics 365 Commerce, která zákazníkům poskytuje lepší přehled o stavu jejich služeb a obchodních funkcích odesíláním telemetrie přímo na zákaznický účet Application Insights.

Povolením funkce Operational Insights pro vaše prostředí v ústředí Commerce Headquarters můžete shromažďovat kurátorovaný seznam událostí jak z Commerce Scale Unit (CSU), tak z vašich zařízení v pokladním místě (POS). Tyto události vám mohou pomoci lépe porozumět, jak fungují vaše systémy a umožňují vám sledovat klíčové technické a obchodní metriky.

I když nechcete tuto telemetrii neustále shromažďovat, můžete rychle povolit nebo zakázat shromažďování pro konkrétní prostředí. Tímto způsobem vám telemetrie může pomoci při odstraňování problémů nebo ladění během vývoje nebo výroby.

## <a name="access-logs-in-application-insights"></a>Přístup k protokolům v Application Insights

Chcete-li získat přístup k protokolům diagnostických událostí pro komponenty Commerce CSU a POS prostřednictvím Application Insights, proveďte postupy v této části.

### <a name="minimum-version-requirements-for-csu"></a>Minimální požadavky na verze pro CSU

CSU má následující minimální požadavky na jednotlivé verze:

- 10.0.23 (Retail Server verze 9.33.22062.15 a novější)
- 10.0.24 (Retail Server verze 9.34.22062.14 a novější)
- 10.0.25 (Retail Server verze 9.35.22062.13 a novější)
- 10.0.26 a novější (všechny verze)

### <a name="enable-diagnostic-events-in-application-insights"></a>Povolení diagnostické události v Application Insights

> [!IMPORTANT]
> Pokud jste dříve používali Operational Insights ve verzi Preview, musíte k aktivaci Operational Insights použít následující postup. Tímto způsobem zajistíte, že spolehlivý a bezpečný přístup k událostem bude moci pokračovat.

Chcete-li povolit události diagnostiky komponent Commerce, musíte mít účet Application Insights. Můžete použít existující účet nebo [vytvořit nový účet](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Z důvodu ochrany osobních údajů doporučujeme používat samostatné účty Application Insights pro provozní, sandboxová a vývojová prostředí. Po vytvoření účtu musíte v centrále povolit funkci **Operational Insights**.

Chcete-li povolit diagnostické události v Application Insights, postupujte takto.

1. V centrále otevřete pracovní prostor **Správa funkcí** a povolte funkci **Operational Insights**.
1. Přejděte na **Správa systému \> Nastavení \> Operational Insights**.
1. Na kartě **Konfigurace** nastavte možnost **Události kanálu Commerce** na **Ano**.
1. Na kartě **Prostředí** zadejte hodnoty **ID prostředí LCS** a **Režim prostředí** pro každé prostředí, kde plánujete používat Application Insights. ID každého prostředí najdete na stránce **Podrobnosti o prostředí** pro dané prostředí v Microsoft Dynamics Lifecycle Services. Tento krok je nutný, aby se zabránilo nechtěnému odeslání diagnostických událostí do nesprávného prostředí při kopírování databází.
1. Na kartě **Registr Application Insights** zadejte hodnotu **Instrumentační klíč** Application Insights a odpovídající hodnotu **Režim prostředí** pro prostředí, ve kterých plánujete používat jednotlivé účty Application Insights.
1. Po dokončení předchozí konfigurace musíte spustit úlohu **CDX Job 1110**. Můžete počkat, až se tato úloha spustí podle vlastního plánu, nebo ji můžete spustit ručně.
1. V Lifecycle Services přejděte na **Podrobnosti o prostředí \> Commerce \> Správa**, vyberte instanci CSU a poté vyberte **Restartovat**. Tento krok opakujte pro každé CSU.
1. Opakujte předchozí kroky pro každé prostředí, kde hodláte použít Application Insights.

> [!NOTE]
> - Události telemetrie v Operational Insights se mohou měnit. Doporučujeme, abyste události Operational Insights používali k provádění předběžné analýzy a odstraňování problémů sami, nikoli k definování řídicích panelů nebo výstrah. Pokud události používáte pro jiné účely než pro samoobslužné odstraňování problémů, doporučujeme ověřit a aktualizovat své dotazy po každém vydání CSU/POS.
> - Od Commerce verze 10.0.29 umožňují postupy v této části také streamování událostí POS Operational Insights na váš účet Application Insights. Další informace naleznete v části [Operational Insights pro POS – události a dotazy](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>K řízení událostí POS Operational Insights použijte soubor DLLHost.exe.config

K použití souboru DLLHost.exe.config pro řízení událostí POS Operational Insights postupujte takto.

1. V textovém editoru otevřete soubor **DLLHost.exe.config** v umístění **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. V sekci **diagnosticsSection** odeberte prvek XML jímky s názvem třídy **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**.
1. Uložit soubor.

### <a name="disable-diagnostic-events-in-application-insights"></a>Zákaz diagnostické události v Application Insights

> [!IMPORTANT]
> Pokud chcete zakázat diagnostické události a již je neodesílat do Application Insights, musíte provést následující postup. Tuto funkci lze zakázat ve Správě funkcí.

Chcete-li zakázat diagnostické události v Application Insights, postupujte takto.

1. V centrále jděte na **Správa systému \> Operational Insights**.
1. Na kartě **Konfigurace** nastavte možnost **Události kanálu Commerce** na **Ne**.
1. Po dokončení předchozí konfigurace musíte spustit úlohu **CDX Job 1110**. Můžete počkat, až se tato úloha spustí podle vlastního plánu, nebo ji můžete spustit ručně.
1. V Lifecycle Services přejděte na **Podrobnosti o prostředí \> Commerce \> Správa**, vyberte instanci CSU a poté vyberte **Restartovat**. Tento krok opakujte pro každé CSU.
1. Opakujte předchozí kroky pro každé prostředí, kde hodláte vypnout Application Insights.

Chcete-li zakázat diagnostické události pro jedno prostředí, odstraňte instrumentační klíč na kartě **Registr Application Insights** na stránce **Operational Insights**. Poté proveďte kroky 3 a 4 předchozího postupu.

> [!NOTE]
> V Commerce verze 10.0.29 a novější kroky v této části také deaktivují streamování událostí POS Operational Insights na váš účet Application Insights. 
