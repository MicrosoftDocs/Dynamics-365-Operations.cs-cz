---
title: Entity aktivit kontejneru
description: Tento článek poskytuje informace o aktivitách kontejneru, které se používají ke sledování postupu přepravních kontejnerů.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: b69d26ee8abaa403f6a0ef3b03d9015fe507dd5b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873949"
---
# <a name="container-activities-entity"></a>Entita aktivit kontejneru

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Kontejnerové aktivity se používají ke sledování postupu přepravních kontejnerů. Pro každý úsek, který je přiřazen k šabloně cesty, která je vybrána při vytváření přepravního kontejneru, se vytvoří záznam. Záznamy se také vytvářejí, když je přepravní kontejner vytvořen prostřednictvím datové entity.

Informace o postupu přepravního kontejneru jsou často přijímány z externího zdroje. Entita aktivit kontejneru umožňuje externímu zdroji, jako je speditér, přímo aktualizovat záznam. Není tedy nutná žádná ruční aktualizace dat.

## <a name="container-activities-itmcontaineractivityentity"></a>Aktivity kontejneru (ITMContainerActivityEntity)

Entitu aktivit kontejneru (`ITMContainerActivityEntity`) můžete použít k vytvoření dalších záznamů o aktivitách. Případně může speditér předat aktualizace pro potvrzenou hodnotu **Skutečné datum ukončení**.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Skutečné datum dokončení | ITMContainerActivityTable.ActualEndDate | Datum a čas | Číslo | Číslo |
| Způsob dodání | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Číslo | Číslo |
| Odhadované datum ukončení | ITMContainerActivityTable.EstimatedDate | Datum a čas | Číslo | Číslo |
| Číslo řádku | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Poznámky | ITMContainerActivityTable.Notes | nvarchar(MAX) | Číslo | Číslo |
| Aktivita | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Číslo | **Ano** |
| Přepravní kontejner | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Ano** | **Ano** |
| Cesta | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Ano** | **Ano** |
| Úsek | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Číslo | **Ano** |
| Poskytovatel služby | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Číslo | Číslo |
| Teplota | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | Číslo | Číslo |
| Plavidlo | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Číslo | Číslo |
| Počáteční datum | ITMContainerActivityTable.StartDate | Datum a čas | Číslo | Číslo |

## <a name="tracking-control"></a>Řízení sledování

Řídicí centrum sledování umožňuje, aby se aktualizace zadaného zdrojového pole spustila aktualizací zadaného cílového pole. Pokud se pomocí entity aktivit kontejneru aktualizuje jak hodnota zdrojového pole, tak hodnota cílového pole, cílové pole zobrazí hodnotu entity. Toto chování souvisí se záznam řízení sledování, které mají v poli **Vytvořit typ** hodnotu *Doba realizace*.

U nákladových oblastí, které mají pole **Vytvořit typ** s hodnotou *Aktualizace stavu* nebo *Prázdný* (což je uživatelem definovaná hodnota), systém aktualizuje stav plavby nebo cílové pole podle konfigurace řízení sledování.

## <a name="calculated-fields"></a>Kalkulovaná pole

Hodnoty následujících polí v záznamu aktivity kontejneru se vypočítají na základě hodnot ostatních polí. Ačkoli tato vypočítaná pole nejsou zahrnuta v datové entitě, budou nastavena, pokud budou poskytnuta pole, na kterých jsou výpočty založeny.

- **Odhadované dny** = **Odhadované datum ukončení** – **Počáteční datum**
- **Skutečné dny** = **Skutečné datum dokončení** – **Počáteční datum**
