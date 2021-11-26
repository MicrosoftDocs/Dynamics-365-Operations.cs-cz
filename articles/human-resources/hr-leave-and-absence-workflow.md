---
title: Vytvoření workflowu žádosti o pracovní volno
description: Vytvoření workflowu žádosti o pracovní volno a absenci pro konzistentní správu žádostí o pracovní volno v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8030e568ac8ef47d8383f09e06ce02a62947698
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728631"
---
# <a name="create-a-leave-request-workflow"></a>Vytvoření workflowu žádosti o pracovní volno

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Workflow v Dynamics 365 Human Resources můžete vytvořit pro účely konzistentní správy žádostí o pracovní volno a absenci. Workflow **pracovní volno a absence** vám umožňuje:

- Definovat úkoly
- Určit, kdo musí dokončit úkoly
- Určit, kdo může schvalovat nebo zamítnout požadavky

## <a name="create-a-leave-and-absence-request-workflow"></a>Vytvoření workflow žádosti o pracovní volno a absenci

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Workflowy lidských zdrojů**.

3. Vyberte **Nový** a poté vyberte **Žádost o pracovní volno a absenci**. 

4. Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.

5. Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno. Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Vytvoření datových prvků workflow žádosti o pracovní volno a absenci

Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o dovolenou a nepřítomnost:

- **Částka**
- **Komentář**
- **Společnost**
- **Vytvořil/a**
- **Datum a čas vytvoření**
- **Datum ukončení**
- **Typ volna**
- **Změnil(a)**
- **Datum a čas úpravy**
- **Kód důvodu**
- **ID požadavku**
- **Datum zahájení**
- **Stav** 
- **Datum odeslání**
- **Odeslal**
- **Odesláno personálním oddělením**
- **Odesláno manažerem**
- **Zadáno jménem**
- **Pracovní podproces**
- **Typ pracovníka**

Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:

- Použijte **Kód důvodu** v podmíněném prohlášení pro směrování žádostí o nemocenskou dovolenou s kódem důvodu **Chirurgická operace** pro předložení HR ke schválení. Všechny ostatní kódy důvodu předkládejte vedoucímu. Další informace o podmíněných příkazech získáte v tématu [Konfigurace podmíněných rozhodnutí ve workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o dovolenou, které tyto role předkládají jménem zaměstnanců. Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
