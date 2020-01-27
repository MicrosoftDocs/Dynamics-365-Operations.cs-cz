---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (5. listopadu 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896766"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (5. listopadu 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2598. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Kopírování instance Core HR

V této týdenní verzi můžete pomocí služby Microsoft Dynamics Lifecycle Services (LCS) kopírovat databázi Microsoft Dynamics 365 Talent: Core HR do prostředí izolovaného prostoru (sandbox). Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox. Další informace naleznete zde:

- [Rozsáhlejší správa prostředí](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)v plánu 2 vlny vydání Dynamics 365: 2019

- [Zkopírování instance Core HR](hr-copy-instance.md) do dokumentace aplikace Talent

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Dávkové úlohy integrace Common Data Service se nevytvoří, když je povolena integrace Common Data Service (388030)

Tato změna vytvoří dávkové úlohy pro integraci Common Data Service, když je povolena.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity nemění velikost obrázku osoby při odeslání (369469)

Verze z tohoto týdne při importu pomocí správy dat změní způsob změny velikosti obrázků pro lepší výkon.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Pozice, která je k dispozici pro datum přiřazení, může předcházet datu aktivace (340103).

Při této změně se zobrazí varování v případě, že vyberete **Dostupné pro datum přiřazení**, které předchází **Datum aktivace pozice**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Nelze vytvořit požadavek na změnu kompenzace v samoobslužných plánech zaměstnanců pro plány založené na kroku (376872).

Tato verze opravuje problém při požadavku na změny kompenzace prostřednictvím samoobslužných stránek zaměstnanců pro plány založené na jednotlivých krocích. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Kód důvodu není synchronizován s Common Data Service, pokud je popis delší než 30 znaků. Core HR umožňuje 60 (352682)

S touto změnou budou v aplikaci Common Data Service aktualizovány kódy důvodů s více než 30 znaky. Změny provedené v Common Data Service se také odrazí v aplikaci Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Řešení integrace z aplikace Talent do Finance and Operations (351961)

Tato verze opravuje problém, kdy adresy aktualizované v aplikaci Talent nebyly aktualizovány v modulu Finance and Operations. Změny v blocích adresy budou nyní aktualizovány.

## <a name="coming-soon"></a>Již brzy

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.

### <a name="feature-management-workspace"></a>Pracovní prostor Správa funkcí

Funkce se přidávají a aktualizují v každém vydání. Funkce Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

Další informace o změnách přicházejících ve správě funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
