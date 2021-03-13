---
title: Vytvoření workflowu žádosti o pracovní volno
description: Vytvoření workflowu žádosti o pracovní volno a absenci pro konzistentní správu žádostí o pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1907ca9cc578737341e52f89453e3d6ae3d0bec
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115045"
---
# <a name="create-a-leave-request-workflow"></a>Vytvoření workflowu žádosti o pracovní volno

Workflow v Dynamics 365 Human Resources můžete vytvořit pro účely konzistentní správy žádostí o pracovní volno a absenci. Workflow **pracovní volno a absence** vám umožňuje:

- Definovat úkoly
- Určit, kdo musí dokončit úkoly
- Určit, kdo může schvalovat nebo zamítnout požadavky

## <a name="create-a-leave-and-absence-request-workflow"></a>Vytvoření workflow žádosti o pracovní volno a absenci

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V části **Nastavení** vyberte **Workflowy lidských zdrojů**.

3. Vyberte **Nový** a poté vyberte **Žádost o pracovní volno a absenci**. 

4. Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.

5. Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno. Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

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

- Použijte **Kód důvodu** v podmíněném prohlášení pro směrování žádostí o nemocenskou dovolenou s kódem důvodu **Chirurgická operace** pro předložení HR ke schválení. Všechny ostatní kódy důvodu předkládejte vedoucímu. Další informace o podmíněných příkazech získáte v tématu [Konfigurace podmíněných rozhodnutí ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o dovolenou, které tyto role předkládají jménem zaměstnanců. Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
