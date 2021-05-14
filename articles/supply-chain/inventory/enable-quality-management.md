---
title: Povolit správu kvality a neshod
description: Toto téma poskytuje přehled procesu pro nastavení a konfiguraci funkcí správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956247"
---
# <a name="enable-quality-and-nonconformance-management"></a>Povolit správu kvality a neshod

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled procesu pro nastavení a konfiguraci funkcí správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Povolit správu kvality a neshod

Chcete-li ve svém systému povolit správu kvality, postupujte podle těchto pokynů.

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry řízení zásob a skladu**.
1. Na kartě **Správa kvality** nastavte možnost **Použít správu kvality** na *Ano*.
1. Do pole **Hodinová sazba** zadejte hodinovou pracovní sazbu v místní měně. Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s neshodou. Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách. S ostatními funkcemi nespolupracují.
1. Vyberte **Nastavení sestavy**.
1. Přidejte nové řádky pro různé typy zpráv a vyberte typ dokumentu, který se má použít pro každou zprávu.
1. Zavřete stránku.
1. Zavřete stránku.

## <a name="quality-management-configuration-process"></a>Proces konfigurace správy kvality

Než začnete používat funkce správy kvality a generovat objednávky kvality, musíte nakonfigurovat systém a předpoklady. Zde je seznam kroků, které jsou nutné ke konfiguraci správy kvality.

1. [Povolit správu kvality a neshod](#enable-qm).
1. Volitelně: [Nakonfigurovat zkušební nástroje](quality-test-instruments.md).
1. [Nakonfigurovat testy](quality-tests.md).
1. [Nakonfigurujte testovací proměnné a výsledky](quality-test-variables.md).
1. [Konfigurujte testovací skupiny](quality-test-groups.md).
1. Volitelné: [Nakonfigurujte skupiny kvality a odkazy na produkty](quality-groups.md).
1. Volitelně: [Nakonfigurujte přidružení kvality](quality-associations.md).

Po dokončení konfigurace můžete začít vytvářet a zpracovávat objednávky kvality. Další informace o vytváření a objednávek kvality a práci s nimi naleznete v tématu [Objednávky kvality](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Proces konfigurace správy neshod

Než začnete používat funkce správy neshod a generovat neshody, musíte nakonfigurovat systém a předpoklady. Zde je seznam kroků, které jsou nutné ke konfiguraci správy neshod.

1. [Povolit správu kvality a neshod](#enable-qm).
1. [Konfigurujte pracovníky, kteří jsou odpovědní za schvalování neshod](quality-responsible-workers.md).
1. [Nakonfigurujte typy problémů](quality-problem-types.md).
1. [Nakonfigurujte karanténní zóny](quality-quarantine-zones.md).
1. [Nakonfigurujte typy diagnostiky](quality-diagnostic-types.md).
1. [Nakonfigurujte operace](quality-operations.md).
1. Volitelně: [Nakonfigurujte poplatky za kvalitu](quality-charges.md).

Po dokončení konfigurace můžete začít vytvářet a zpracovávat neshody. Další informace o vytvoření neshod a práci s nimi naleznete v tématu [Vytvoření a zpracování neshod](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
