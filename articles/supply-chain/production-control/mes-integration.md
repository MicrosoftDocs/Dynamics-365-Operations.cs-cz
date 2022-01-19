---
title: Integrace s výrobními informačními systémy třetích stran
description: Toto téma vysvětluje, jak můžete integrovat Microsoft Dynamics 365 Supply Chain Management s výrobním informačním systémem třetí strany (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ea39a1fc9092aaa4622c7193f7538acc85aa0f46
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952670"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integrace s výrobními informačními systémy třetích stran

[!include [banner](../includes/banner.md)]

Některé výrobní organizace, které používají Microsoft Dynamics 365 Supply Chain Management, využívají nativní funkce Dynamics 365 k řízení jejich výrobních činností u strojů, zařízení a personálu. Jiné výrobní organizace, zejména ty, které mají pokročilé požadavky na výrobu, však místo toho používají výrobní informační systém (MES) třetí strany. Organizace si mohou vybrat řešení MES třetí strany, protože je například specificky přizpůsobeno jejich vertikálnímu odvětví.

V integrovaném řešení je výměna dat plně automatizovaná a probíhá téměř v reálném čase. Proto jsou data v obou systémech aktuální a není potřeba žádné ruční zadávání dat. Když je například spotřeba materiálu registrována v MES, integrace zajišťuje, že stejná spotřeba je zaregistrována také v Dynamics 365. Proto jsou aktuální skladové záznamy k dispozici dalším důležitým procesům, jako je plánování a prodej.

Toto řešení umožňuje uživatelům Supply Chain Management rychlejší, jednodušší a levnější integraci s MES třetích stran. Nabízí následující funkce:

- Obchodní akce a rozhraní, která podporují [klíčové výrobní informační procesy](#processes-available-for-mes-integration)
- Centralizovaný řídicí panel, kde můžete sledovat historii zpracování událostí a odstraňovat problémy a opravovat procesy, které selžou

Následující obrázek ukazuje typickou kolekci obchodních událostí, procesů a zpráv, které se vyměňují v integrovaném řešení.

![Typický scénář integrace.](media/3p-mes-scenario.png "Typický scénář integrace.")

## <a name="turn-on-the-mes-integration-feature"></a>Zapnutí funkce integrace MES

Než budete moci používat tuto funkci, musí ji správce v systému zapnout, jak je popsáno v následujícím tématu.

1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Ujistěte se, že je aktivní licenční klíč **Čas a docházka** (zobrazuje se zaškrtnutí). Tento licenční klíč je vyžadován, protože řídí funkčnost a data výrobního systému. Pokud není aktivní, proveďte následující kroky:
    1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Na stránce **Konfigurace licence** zaškrtněte políčko **Čas a docházka**.
    1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Zapněte funkci, která je uvedena následovně (viz též [Přehled správy funkce](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Modul:** *Řízení výroby*
    - **Název funkce:** *Integrace výrobního informačního systému*

## <a name="processes-available-for-mes-integration"></a>Dostupné procesy pro integraci MES

Pro integraci můžete povolit kterýkoli nebo všechny z následujících procesů.

| Název procesu | Popis |
|---|---|
| Uvolnění výrobních zakázek a obchodní události změny stavu výrobní zakázky | Tento proces poskytuje obchodní událost, které může MES naslouchat, aby získal informace o výrobních zakázkách, které by měly být vyrobeny. Očekává se, že referenční data, která se vztahují k výrobní zakázce, budou sdílena ze Supply Chain Management do MES prostřednictvím protokolu OData (Open Data Protocol) nebo datových entit. |
| Spustit výrobní zakázku | Tento proces poskytuje aplikaci Supply Chain Management informace o výrobních zakázkách, které jsou spuštěny prostřednictvím MES. Zajišťuje, aby oba systémy měly aktuální přehled o všech výrobních činnostech. |
| Vykazování vyrobeného nebo zlikvidovaného množství | Tento proces poskytuje aplikaci Supply Chain Management informace o množství kvalitních a chybných položek, které jsou vykazovány u výrobního úkolu prostřednictvím MES. Zajišťuje, aby vedoucí výroby měli aktuální přehled o průběhu výrobního plánu. |
| Vykazování spotřeby surovin | Tento proces poskytuje aplikaci Supply Chain Management informace z MES o množství spotřebovaných materiálů. Zpřístupňuje aktuální skladové záznamy dalším důležitým procesům, jako je plánování a prodej. |
| Vykazování času spotřebovaného na operaci | Tento proces poskytuje aplikaci Supply Chain Management informace o čase, který se používá pro konkrétní operaci. |
| Ukončit výrobní zakázku | Tento proces informuje Supply Chain Management, že MES aktualizoval výrobní zakázku na její konečný stav *Ukončeno*. Tento stav znamená, že na výrobní zakázce již nebudou přibývat žádná další množství. |

## <a name="monitor-incoming-messages"></a>Sledování příchozích zpráv

Chcete-li sledovat příchozí zprávy do systému, otevřete stránku **Integrace výrobních informačních systémů**. Zde můžete prohlížet, zpracovávat a odstraňovat problémy.

## <a name="call-the-api"></a>Volání rozhraní API

Chcete-li volat rozhraní API pro integraci MES, odešlete požadavek `POST` na následující adresu URL koncového bodu:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Tělo požadavku, který odešlete, by mělo připomínat následující příklad. Hodnoty `_companyId`, `_messageType` a `_messageContent` nahraďte svými údaji podle potřeby. Informace o různých typech zpráv, které rozhraní API podporuje, a o tom, jak navrhnout jejich obsah, naleznete v další části.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>Typy a obsah zpráv API

Tato část popisuje jednotlivé typy zpráv, které lze vyměňovat prostřednictvím rozhraní API pro integraci MES.

### <a name="start-production-order-message"></a>Zpráva o spuštění výrobní zakázky

U zprávy *spuštění výrobní zakázky* má údaj `_messageType` hodnotu `ProdProductionOrderStart`. Následující tabulka ukazuje pole, která tato zpráva podporuje.

| Název pole | Stav | Typ |
|---|---|---|
| `ProductionOrderNumber` | Povinné | Řetězec |
| `StartedQuantity` | Volitelné | Reálný |
| `StartedDate` | Volitelné | Datum |
| `AutomaticBOMConsumptionRule` | Volitelné | Enum (FlushingPrincip \| Always \| Never) |

### <a name="report-as-finished-message"></a>Zpráva Vykázat jako dokončené

U zprávy *vykázat jako dokončené* má údaj `_messageType` hodnotu `ProdProductionOrderReportFinished`. Následující tabulka ukazuje pole, která tato zpráva podporuje.

| Název pole | Stav | Typ |
|---|---|---|
| `ProductionOrderNumber` | Povinné | Řetězec |
| `ReportFinishedLines` | Povinné | Seznam řádků (alespoň jeden), z nichž každý obsahuje datovou část, která je popsána v následující tabulce |

Následující tabulka ukazuje pole, která jsou podporována v každém řádku oddílu `ReportFinishedLines` ve zprávě `ProdProductionOrderReportFinished`.

| Název pole | Stav | Typ |
|---|---|---|
| `LineNumber` | Volitelné | Reálný |
| `ItemNumber` | Volitelné | Řetězec|
| `ProductionType` | Volitelné | Enum (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None), rozšiřitelné |
| `ReportedErrorQuantity` | Volitelné | Reálný|
| `ReportedGoodQuantity` | Volitelné | Reálný|
| `ReportedErrorCatchWeightQuantity` | Volitelné | Reálný |
| `ReportedGoodCatchWeightQuantity` | Volitelné | Reálný |
| `AcceptError` | Volitelné |Logická |
| `ErrorCause` | Volitelné | Enum (None \| Material \| Machine \| OperatingStaff), rozšiřitelné |
| `ExecutedDateTime` | Volitelné | Datum/čas |
| `ReportAsFinishedDate` | Volitelné | Datum |
| `AutomaticBOMConsumptionRule` | Volitelné | Enum (FlushingPrincip \| Always \| Never) |
| `AutomaticRouteConsumptionRule` | Volitelné |Enum (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | Volitelné | Logická |
| `ProductionJournalNameId` | Volitelné | Řetězec |
| `PickingListProductionJournalNameId` | Volitelné | Řetězec|
| `RouteCardProductionJournalNameId` | Volitelné | Řetězec |
| `FromOperationNumber` | Volitelné | Celé číslo|
| `ToOperationNumber` | Volitelné | Celé číslo|
| `InventoryLotId` | Volitelné | Řetězec |
| `BaseValue` | Volitelné | Řetězec |
| `EndJob` | Volitelné | Logická |
| `EndPickingList` | Volitelné | Logická |
| `EndRouteCard` | Volitelné | Logická |
| `PostNow` | Volitelné | Logická |
| `AutoUpdate` | Volitelné | Logická |
| `ProductColorId` | Volitelné | Řetězec|
| `ProductConfigurationId` | Volitelné | Řetězec |
| `ProductSizeId` | Volitelné | Řetězec |
| `ProductStyleId` | Volitelné | Řetězec |
| `ProductVersionId` | Volitelné | Řetězec |
| `ItemBatchNumber` | Volitelné | Řetězec |
| `ProductSerialNumber` | Volitelné | Řetězec |
| `LicensePlateNumber` | Volitelné | Řetězec |
| `InventoryStatusId` | Volitelné | Řetězec |
| `ProductionWarehouseId` | Volitelné | Řetězec |
| `ProductionSiteId` | Volitelné | Řetězec |
| `ProductionWarehouseLocationId` | Volitelné | Řetězec |
| `InventoryDimension1` do `InventoryDimension12` | Volitelné | Řetězec |

12 rozšiřitelných dimenzí (`InventoryDimension1` až `InventoryDimension12`) vyžaduje přizpůsobení a nejsou vždy používány. Více informací o nich najdete v tématu [Přidání nových dimenzí zásob prostřednictvím rozšíření](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Zpráva o spotřebě materiálu (výdejka)

U zprávy *spotřeba materiálu (výdejka)* má údaj `_messageType` hodnotu `ProdProductionOrderPickingList`. Následující tabulka ukazuje pole, která tato zpráva podporuje.

| Název pole | Stav | Typ |
|---|---|---|
| `ProductionOrderNumber` | Povinné | Řetězec |
| `JournalNameId` | Volitelné | Řetězec |
| `PickingListLines` | Povinné | Seznam řádků (alespoň jeden), z nichž každý obsahuje datovou část, která je popsána v následující tabulce |

Následující tabulka ukazuje pole, která jsou podporována v každém řádku oddílu `PickingListLines` ve zprávě `ProdProductionOrderPickingList`.

| Název pole | Stav | Typ |
|---|---|---|
| `ItemNumber` | Povinné | Řetězec |
| `ConsumptionBOMQuantity` | Volitelné | Reálný |
| `ProposalBOMQuantity` | Volitelné | Reálný |
| `ScrapBOMQuantity` | Volitelné | Reálný |
| `BOMUnitSymbol` | Volitelné | Řetězec |
| `ConsumptionInventoryQuantity` | Volitelné | Reálný |
| `ProposalInventoryQuantity` | Volitelné | Reálný |
| `ConsumptionCatchWeightQuantity` | Volitelné | Reálný |
| `ProposalCatchWeightQuantity` | Volitelné | Reálný |
| `ConsumptionDate` | Volitelné | Datum |
| `OperationNumber` | Volitelné | Celé číslo |
| `LineNumber` | Volitelné | Reálný |
| `PositionNumber` | Volitelné | Řetězec |
| `IsConsumptionEnded` | Volitelné | Logická |
| `ErrorCause` | Volitelné | Enum (None \| Material \| Machine \| OperatingStaff), rozšiřitelné |

### <a name="time-used-for-operation-route-card-message"></a>Zpráva Čas použitý pro operaci (karta postupu)

U zprávy *čas potřebný k operaci (karta postupu)* má údaj `_messageType` hodnotu `ProdProductionOrderRouteCard`. Následující tabulka ukazuje pole, která tato zpráva podporuje.

| Název pole | Stav | Typ |
|---|---|---|
| `ProductionOrderNumber` | Povinné | Řetězec |
| `JournalNameId` | Volitelné | Řetězec |
| `RouteCardLines` | Povinné | Seznam řádků (alespoň jeden), z nichž každý obsahuje datovou část, která je popsána v následující tabulce |

Následující tabulka ukazuje pole, která jsou podporována v každém řádku oddílu `RouteCardLines` ve zprávě `ProdProductionOrderRouteCard`.

| Název pole | Stav | Typ |
|---|---|---|
| `OperationNumber` | Povinné | Celé číslo |
| `OperationPriority` | Volitelné | Enum (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | Volitelné | Řetězec |
| `OperationsResourceId` | Volitelné | Řetězec |
| `Worker` | Volitelné | Řetězec |
| `HoursRouteCostCategoryId` | Volitelné | Řetězec |
| `QuantityRouteCostCategoryId` | Volitelné | Řetězec |
| `HourlyRate` | Volitelné | Reálný |
| `Hours` | Volitelné | Reálný |
| `GoodQuantity` | Volitelné | Reálný |
| `ErrorQuantity` | Volitelné | Reálný |
| `CatchWeightGoodQuantity` | Volitelné | Reálný |
| `CatchWeightErrorQuantity` | Volitelné | Reálný |
| `QuantityPrice` | Volitelné | Reálný |
| `ProcessingPercentage` | Volitelné | Reálný |
| `ConsumptionDate` | Volitelné | Datum |
| `TaskType` | Volitelné | Enum (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | Volitelné | Enum (None \| Material \| Machine \| OperatingStaff), rozšiřitelné |
| `OperationCompleted` | Volitelné | Logická |
| `BOMConsumption` | Volitelné | Logická |
| `ReportAsFinished` | Volitelné | Logická |

### <a name="end-production-order-message"></a>Zpráva o ukončení výrobní zakázky

U zprávy *ukončení výrobní zakázky* má údaj `_messageType` hodnotu `ProdProductionOrderEnd`. Následující tabulka ukazuje pole, která tato zpráva podporuje.

| Název pole | Stav | Typ |
|---|---|---|
| `ProductionOrderNumber` | Povinné | Řetězec |
| `ExecutedDateTime` | Volitelné | Datum/čas |
| `EndedDate` | Volitelné | Datum |
| `UseTimeAndAttendanceCost` | Volitelné | Logická |
| `AutoReportAsFinished` | Volitelné | Logická |
| `AutoUpdate` | Volitelné | Logická |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Získání zpětné vazby o stavu zprávy

Poté, co MES odešle zprávu do aplikace Supply Chain Management, může být důležité, aby Supply Chain Management vrátila zpětnou vazbu o stavu zprávy. Zde je několik příkladů, kdy může být toto chování relevantní:

- Neexistuje žádná osoba, která zodpovídá za neustálý dohled nad integrací MES.
- Osoba, která je zodpovědná za dohled nad integrací MES, chce být informována e-mailem, když zpráva selže, aby věděla, že musí jednat.
- MES musí zobrazit chybovou zprávu, aby informoval operátora dílny nebo někoho z IT oddělení, že musí podniknout určitou akci.
- MES musí přepočítat plán objednávky poté, co obdrží zprávu o selhání (například proto, že se nepodařilo spustit výrobní zakázku).

V těchto případech můžete využít standardní funkci výstrahy v Supply Chain Management. Informace o tom, jak fungují standardní výstrahy, naleznete v následujících zdrojích:

- Téma nápovědy: [Přehled výstrah](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Možnosti pravidla výstrahy v Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Můžete například nastavit následující výstrahy, abyste poskytli zpětnou vazbu o stavu zprávy:

- Vytvořte obchodní událost ("Odeslat externě"), která se použije, když zpráva obsahuje text *Chyba*.
- Odešlete oznámení a e-mail správci IT nebo vedoucímu výroby.
