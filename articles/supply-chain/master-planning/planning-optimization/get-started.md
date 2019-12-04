---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773915"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Začínáme s optimalizací plánování

Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Microsoft Dynamics 365 Supply Chain Management. Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům. Ve výchozím nastavení není funkce optimalizace plánování zapnuta ve službě Lifecycle Services (LCS). Proto máte příležitost provést vyhodnocení před tím, než ji zapnete.

Případně optimalizace plánování nahradí předdefinovaný modul plánování Supply Chain Management.

Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)

### <a name="licensing"></a>Licencování

Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.

### <a name="install-the-add-in"></a>Instalace doplňku

Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management. Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.

1. Přihlaste se k LCS a otevřete požadované prostředí.
1. Přejděte na **Úplné podrobnosti**.
1. Vyberte **Správa** nebo přejděte na pevnou záložku **Doplňky prostředí**.
1. Vyberte možnost **Nainstalovat nový doplněk**.
1. Vyberte **Optimalizace plánování**.
1. Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.
1. Vyberte **Instalovat**.

### <a name="planning-optimization-integration"></a>Integrace optimalizace plánování

Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Integrace optimalizace plánování** \> **Parametry integrace**.

#### <a name="connection-status"></a>Stav připojení

Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování. Následující tabulka zobrazuje možné hodnoty.

| Stav připojení | Popis | Lze používat optimalizaci plánování? |
|---|---|---|
| Připojeno | Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management. | Ano |
| Povolení připojení | Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá. | Ne |
| Odpojeno | Neexistuje připojení ke službě optimalizace plánování. Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu. | Ne |
| Zakazování připojení | Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá. | Ne |
| Načítání stavu | Systém čeká na informace o stavu ze služby optimalizace plánování. | Ne |

#### <a name="the-use-planning-optimization-option"></a>Možnost použití optimalizace plánování

Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:

- **Ano** – optimalizace plánování se používá pro hlavní plánování.
- **Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management

> [!NOTE]
> Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.

### <a name="integration-with-the-setup"></a>Integrace s nastavením

Je-li zapnut náhled optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování. V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.

## <a name="related-resources"></a>Související prostředky

[Podmínky a ustanovení pro náhled](https://go.microsoft.com/fwlink/?linkid=2015274)

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)
