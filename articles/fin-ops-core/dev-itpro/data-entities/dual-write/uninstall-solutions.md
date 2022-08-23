---
title: Odinstalace řešení pro orchestraci aplikace s duálním zápisem
description: Tento článek popisuje, jak odinstalovat řešení pro orchestraci aplikací s duálním zápisem.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: fd9dc98ec1323a2ef262a330a400a6bd3833e554
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288723"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Odinstalace řešení pro orchestraci aplikace s duálním zápisem

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak odinstalovat řešení pro orchestraci aplikací s duálním zápisem.

Někteří zákazníci si neúmyslně nainstalují balíček pro orchestraci aplikací s duálním zápisem, který do prostředí Microsoft Dataverse nainstaluje více řešení. Instalace nadbytečných řešení v balíčku může způsobit neočekávané a nežádoucí problémy.

Chcete-li vyřešit problémy související s instalací balíčku pro orchestraci aplikací s duálním zápisem, odinstalujte nechtěná řešení s duálním zápisem v následujícím pořadí:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (pokud existuje)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Chcete-li toto řešení odinstalovat, musíte otevřít lístek podpory u společnosti Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Pokud byla nainstalována řešení strany a globálního adresáře, odinstalujte řešení v následujícím pořadí:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Strana
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
