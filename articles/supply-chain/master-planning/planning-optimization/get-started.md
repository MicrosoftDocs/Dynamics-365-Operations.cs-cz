---
title: Začínáme s hlavním plánováním
description: Tento článek vysvětluje, jak používat funkci hlavního plánování v Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780405"
---
# <a name="get-started-with-master-planning"></a>Začínáme s hlavním plánováním

[!include [banner](../../includes/banner.md)]

Hlavní plánování v Supply Chain Management zajišťuje externí služba nazvaná Doplněk optimalizace plánování pro Dynamics 365 Supply Chain Management. Toto téma vysvětluje, jak získat a nastavit tuto službu.

## <a name="availability"></a>Dostupnost

Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Brazílie, Evropa, Francie, Spojené království, Norsko, Švýcarsko, Austrálie, Asie a Tichomoří, Japonsko a Indie. Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována. Další informace o geografických oblastech Azure a souvisejících oblastech najdete v tématu [Geografické oblasti Azure](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Licence

Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.

## <a name="install-and-enable-planning-optimization"></a>Instalace a povolení optimalizace plánování

Chcete-li použít optimalizaci plánování, musí mít systém zavedené všechny předpoklady a poté povolit svůj licenční klíč a nainstalovat doplněk Optimalizace plánování pro Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Předpoklady

Před instalací doplňku Optimalizace plánování musí být splněny následující předpoklady:

- Musíte používat Supply Chain Management v LCS aktivovaném prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější. Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.

- Váš systém musí být nastaven na integraci Power Platform. Další informace naleznete v tématu [Integrace Microsoft Power Platform s finančními a provozními aplikacemi](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Povolení licence Optimalizace plánování

Chcete-li použít optimalizaci plánování, musíte povolit její konfigurační klíč. Postup je následující:

1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Na kartě **Konfigurační klíče** zaškrtněte políčko **Optimalizace plánování**.
1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Instalace doplňku optimalizace plánování

Musíte instalovat doplněk z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.

Instalace doplňku optimalizace plánování:

1. Přihlaste se k LCS a otevřete požadované prostředí.
1. Přejděte na **Úplné podrobnosti**.
1. Přejděte na záložku s náhledem **Doplňky prostředí**.
1. Vyberte možnost **Nainstalovat nový doplněk**.
1. Vyberte **Optimalizace plánování**.
1. Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.
1. Vyberte **Instalovat**.
1. Na záložce s náhledem **Doplňky prostředí** by se mělo zobrazit, že se instaluje optimalizace plánování.
1. Po několika minutách by se měla položka **Instaluje se** změnit na **Nainstalováno** (pravděpodobně bude nutné aktualizovat stránku). Po instalaci můžete aktivovat optimalizaci plánování v aplikaci Dynamics 365 Supply Chain Management.

Hlavním účelem instalace doplňku Optimalizace plánování je propojení služby a prostředí. Proto musíte doplněk nainstalovat samostatně do každého prostředí, kde budete používat optimalizaci plánování, bez ohledu na jakýkoli kód přesunutý mezi prostředími.

## <a name="integrate-planning-optimization-with-your-system"></a>Integrace optimalizace plánování do systému

Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.

### <a name="connection-status"></a>Stav připojení

Stav připojení označuje aktuální stav spojení mezi Supply Chain Management a službou optimalizace plánování. Následující tabulka zobrazuje možné hodnoty.

| Stav připojení | Popis | Lze používat optimalizaci plánování? |
|---|---|---|
| Připojeno | Bylo navázáno spojení mezi službou optimalizace plánování a Supply Chain Management. | Ano |
| Povolení připojení | Požadavek na zapnutí připojení ke službě optimalizace plánování právě probíhá. | Ne |
| Odpojeno | Neexistuje připojení ke službě optimalizace plánování. Připojení lze zapnout z LCS, jak je popsáno výše v tomto článku. | Číslo |
| Zakazování připojení | Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá. | Ne |
| Načítání stavu | Systém čeká na informace o stavu ze služby optimalizace plánování. | Ne |

### <a name="the-use-planning-optimization-option"></a>Možnost použití optimalizace plánování

Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:

- **Ano** – optimalizace plánování se používá pro hlavní plánování.
- **Ne** – pro hlavní plánování se používá zastaralý modul hlavního plánování.

Toto nastavení platí pro všechny právnické osoby (společnosti). Optimalizaci plánování není možné použít u některých právnických osob a zastaralý modul hlavního plánování u jiných právnických osob.

> [!NOTE]
> Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro zastaralý modul hlavního plánování, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.

### <a name="integration-with-the-setup"></a>Integrace s nastavením

Je-li zapnuta optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování. V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
