---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8681ef80166f7d5f108c9424b53fa5c6f5324467
ms.sourcegitcommit: fcb1aa39e933216dea9e586b552bce6057f416a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2021
ms.locfileid: "7645775"
---
# <a name="get-started-with-planning-optimization"></a>Začínáme s optimalizací plánování

[!include [banner](../../includes/banner.md)]

Tak jak bylo [dříve oznámeno](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), optimalizace plánování nahradí stávající integrovaný hlavní plánovací modul.

Pokud aktuálně používáte integrovaný hlavní plánovací modul, měli byste nyní začít plánovat migraci na optimalizaci plánování. Je důležité zahájit proces migrace co nejdříve, protože při vynucení ukončení podpory může dojít k ovlivnění vašich operací. Abyste se vyhnuli problémům na poslední chvíli při vynuceném ukončení podpory, důrazně doporučujeme dokončit migraci před 1. prosincem 2020. 

Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Supply Chain Management. Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům. Funkce Optimalizace plánování není ve výchozím nastavení ve službě Dynamics Lifecycle Services (LCS) zapnutá, takže si ji můžete před zapnutím vyhodnotit.

> [!NOTE]
> Pokud váš hlavní plánovací proces nezahrnuje produkci (hlavní plánování generovalo plánované výrobní zakázky) a vyžadujete vestavěný hlavní plánovací stroj verze vyšší než 10.0.15, musíte požádat o výjimku z migrace na optimalizaci plánování. Počínaje verzí 10.0.16 se v prostředích zobrazí chyba při spuštění integrovaného hlavního plánování bez generování plánovaných výrobních zakázek. Optimalizace plánování by se měla použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky. Vlastníci stávajících prostředí, na nichž běží vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky. Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.

Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)

## <a name="availability"></a>Dostupnost

Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Spojené království, Austrálie, Asie a Tichomoří a Japonsko. Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována. Další informace o geografických oblastech Azure a souvisejících oblastech najdete v tématu [Geografické oblasti Azure](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Licence

Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.

## <a name="install-and-enable-planning-optimization"></a>Instalace a povolení optimalizace plánování

Chcete-li použít optimalizaci plánování, musí mít systém zavedené všechny předpoklady a poté povolit svůj licenční klíč a nainstalovat doplněk Optimalizace plánování pro Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Předpoklady

Před instalací doplňku Optimalizace plánování musí být splněny následující předpoklady:

- Musíte používat Supply Chain Management v LCS aktivovaném prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější. Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.

- Váš systém musí být nastaven na integraci Power Platform. Další informace naleznete v tématu [Integrace Microsoft Power Platform s aplikacemi Finance and Operations](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

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
| Odpojeno | Neexistuje připojení ke službě optimalizace plánování. Připojení lze zapnout z LCS, jak je popsáno výše v tomto tématu. | Ne |
| Zakazování připojení | Požadavek na vypnutí připojení ke službě optimalizace plánování právě probíhá. | Ne |
| Načítání stavu | Systém čeká na informace o stavu ze služby optimalizace plánování. | Ne |

### <a name="the-use-planning-optimization-option"></a>Možnost použití optimalizace plánování

Nastavení možnosti **Použít optimalizaci plánování** určuje, který plánovací modul se použije pro hlavní plánování:

- **Ano** – optimalizace plánování se používá pro hlavní plánování.
- **Ne** – pro hlavní plánování se používá integrovaný modul Supply Chain Management

Toto nastavení platí pro všechny právnické osoby (společnosti). Optimalizaci plánování není možné použít u některých právnických osob a integrované hlavní plánování u jiných právnických osob.

> [!NOTE]
> Pokud jsou aktivovány stávající dávkové úlohy plánování, které byly vytvořeny pro předdefinovaný modul plánování Supply Chain Management, zatímco možnost **Použít optimalizaci plánování** je nastavena na hodnotu **Ano**, tyto úlohy se nezdaří.

### <a name="integration-with-the-setup"></a>Integrace s nastavením

Je-li zapnuta optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování. V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.

## <a name="additional-resources"></a>Další prostředky

[Podmínky a ustanovení pro náhled](https://go.microsoft.com/fwlink/?linkid=2015274)

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
