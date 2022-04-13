---
title: Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna
description: Vytvpřte pracovního postupu žádosti o koupi a prodej pracovního volna pro konzistentní správu koupi a prodeje pracovního volna v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f200fec48dc6bff2702b962c47cbd6951c5921c
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509409"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna


>[!Important]
>Funkce uvedené v tomto tématu jsou aktuálně dostupné pro zákazníky používající samostatnou verzi aplikace Dynamics 365 Human Resources. Některé nebo všechny funkce budou dostupné jako součást budoucího vydání na infrastruktury Finance po vydání Finance 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V aplikaci Dynamics 365 Human Resources můžete vytvořit pracovní postup pro účely konzistentní správy žádostí o koupi a prodej pracovního volna. Pracovní postup **Koupě a prodej pracovního volna** vám umožňuje:

- Definovat úkoly
- Určit, kdo musí dokončit úkoly
- Určit, kdo může schvalovat nebo zamítnout požadavky

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Workflowy lidských zdrojů**.

3. Vyberte **Nový** a poté vyberte **Žádost o koupi a prodej pracovního volna**. 

4. Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.

5. Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno. Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Vytvoření datových prvků workflow žádosti o pracovní volno a absenci

Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o koupi a prodej pracovního volna:

- **Částka**
- **Zásady nákupu a prodeje pracovního volna**
- **Společnost**
- **Vytvořil**
- **Datum a čas vytvoření**
- **Koncové datum**
- **Typ pracovního volna**
- **Změnil/a**
- **Datum a čas úpravy**
- **ID požadavku**
- **Datum zahájení**
- **Stav** 
- **Datum odeslání**
- **Odeslal/a**
- **Odesláno personálním oddělením**
- **Odesláno manažerem**
- **Zadáno jménem**
- **Pracovní podproces**

## <a name="workflow-examples"></a>Příklady pracovních postupů

Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:

- Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o koupi a prodej pracovního volna, které tyto role předkládají jménem zaměstnanců. Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.

## <a name="see-also"></a>Viz také

[Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)<br>
[Správa zásad nákupu a prodeje pracovního volna](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Koupit a prodat pracovní volno](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
