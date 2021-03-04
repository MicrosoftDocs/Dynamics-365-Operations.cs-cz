---
title: Začínáme s optimalizací plánování
description: Toto téma vysvětluje, jak používat funkci Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424259"
---
# <a name="get-started-with-planning-optimization"></a>Začínáme s optimalizací plánování

[!include [banner](../../includes/banner.md)]

Tak jak bylo [dříve oznámeno](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), optimalizace plánování nahradí stávající integrovaný hlavní plánovací modul.

Pokud aktuálně používáte integrovaný hlavní plánovací modul, měli byste nyní začít plánovat migraci na optimalizaci plánování. Je důležité zahájit proces migrace co nejdříve, protože při vynucení ukončení podpory může dojít k ovlivnění vašich operací. Abyste se vyhnuli problémům na poslední chvíli při vynuceném ukončení podpory, důrazně doporučujeme dokončit migraci před 1. prosincem 2020. 

Funkce Optimalizace plánování aktuálně nepodporuje všechny funkce, které jsou k dispozici v modulu plánování integrovaném v aplikaci Supply Chain Management. Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici v optimalizaci plánování, bude vyhovovat vašim požadavkům. Funkce Optimalizace plánování není ve výchozím nastavení ve službě Dynamics Lifecycle Services (LCS) zapnutá, takže si ji můžete před zapnutím vyhodnotit.

> [!NOTE]
> Pokud váš hlavní plánovací proces nezahrnuje produkci (hlavní plánování generovalo plánované výrobní zakázky) a vyžadujete vestavěný hlavní plánovací stroj verze vyšší než 10.0.15, musíte požádat o výjimku z migrace na optimalizaci plánování. Počínaje verzí 10.0.16 se v prostředích zobrazí chyba při spuštění integrovaného hlavního plánování bez generování plánovaných výrobních zakázek. Optimalizace plánování by se měla použít pro všechna nová nasazení, která během generování plánování negenerují plánované výrobní zakázky. Vlastníci stávajících prostředí, na nichž běží vestavěný hlavní plánovací modul bez generování plánovaných výrobních zakázek, obdrží e-mail s podrobnostmi o procesu výjimky. Doporučujeme, abyste při hodnocení a plánování migrace na optimalizaci plánování spolupracovali s partnerem.

Než zapnete optimalizaci plánování, důrazně doporučujeme, abyste vyhodnotili výsledky analýzy podle optimalizace plánování. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)

### <a name="availability"></a>Dostupnost
Optimalizace plánování je v současné době k dispozici v následujících geografických oblastech Azure: USA, Kanada, Evropa, Velká Británie a Austrálie. Pokud se pokusíte nainstalovat doplněk z jiné geografické oblasti, LCS zobrazí zprávu, že tato geografická oblast není podporována.

Všimněte si, že optimalizace plánování nepodporuje místní nasazení Dynamics 365 Supply Chain Management.

### <a name="licensing"></a>Licence

Pokud lze spustit hlavní plánování pomocí aktuální licence, nemusíte kupovat další licenci, aby bylo možné začít používat optimalizaci plánování.

### <a name="install-the-add-in"></a>Instalace doplňku

Chcete-li použít optimalizaci plánování, nainstalujte doplněk Optimalizace plánování pro aplikaci Dynamics 365 Supply Chain Management. Můžete získat přístup k doplňku z projektu LCS a zapnout funkci optimalizace plánování z uživatelského rozhraní (UI) Supply Chain Management.

> [!NOTE]
> Požadavek optimalizace plánování je LCS aktivované prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější. Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace se nedokončí a budete ji muset zrušit.

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

### <a name="planning-optimization-integration"></a>Integrace optimalizace plánování

Chcete-li nakonfigurovat, zda by měl být pro hlavní plánování použit doplněk Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Parametry optimalizace plánování**.

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

Je-li zapnuta optimalizace plánování, hlavní plánování se provede pomocí doplňku optimalizace plánování. V tomto případě budou ovlivněny výsledky a funkce hlavního plánování.

## <a name="additional-resources"></a>Další prostředky

[Podmínky a ustanovení pro náhled](https://go.microsoft.com/fwlink/?linkid=2015274)

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]