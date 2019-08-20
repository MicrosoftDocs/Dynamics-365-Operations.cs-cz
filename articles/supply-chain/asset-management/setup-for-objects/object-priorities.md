---
title: Úrovně služby Majetek
description: V tomto tématu jsou vysvětleny úrovně služby Majetek v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783132"
---
# <a name="asset-service-levels"></a>Úrovně služby Majetek

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V tomto tématu jsou vysvětleny úrovně služby Majetek v modulu Správa majetku. Úrovně služby Majetek jsou spojeny s majetkem a jsou převedeny do požadavků na údržbu a pracovních příkazů. Používají se k výpočtu priority pracovních příkazů během plánování pracovních příkazů. Úrovně služby majetek lze změnit, pokud jsou požadovány změny.

Další informace o nastavení, které souvisí s výpočtem skóre hodnocení pro plánování pracovních příkazů, naleznete v tématu [Parametry Správy majetku](../setup-for-objects/enterprise-asset-management-parameters.md). Je nutné nastavit alespoň jeden výchozí záznam pro úroveň služby Majetek. Tento výchozí záznam se používá v případě, že během plánování pracovních příkazů nebyla nalezena žádná jiná shoda.

**Příklad 1:** výchozí úroveň služby, která se používá v případě, že nebyla nalezena žádná jiná shoda. V tomto záznamu vyberete pouze úroveň služby.

**Příklad 2:** vysoká úroveň služby, která slouží k naplánování prací pro motor kamionu Volvo. V tomto záznamu vyberete příslušný typ majetku (například **Motor nákladního vozu**), výrobce (**Volvo**) a úroveň služby.

## <a name="set-up-asset-service-levels"></a>Nastavení úrovní služby Majetek

1. Vyberte **Správa majetku** \> **Nastavení** \> **Úrovně služby Majetek**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. V závislosti a úrovni podrobností vyžadované pro úroveň služeb majetku proveďte příslušné výběry v polích **Funkční umístění**, **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Typ pracovního příkazu** a **Úroveň služby**.

    > [!NOTE]
    > Pokud je úroveň služby Majetek použita pro požadavky na údržbu a pracovní příkazy, bude správa majetku procházet všemi záznamy o úrovni služby Majetek, aby zkontrolovala možnou shodu. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, Správa majetku nejprve zkontroluje shodu v poli **Typ pracovního příkazu**. Pokud není nalezena shoda, zkontroluje shodu v poli **Majetek** a tak dále. Jak vidíte v rozvržení stránky **Úrovně služby Majetek**, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody. Není-li nalezena shoda, použije se výchozí záznam, který nemá žádné výběry v těchto polích.

4. V poli **Úroveň služby** vyberte číslo označující úroveň služby (priorita).


> [!NOTE]
> Pokud změníte záznam úrovně služby Majetek na stránce **Úrovně služby Majetek** poté, co jste jej již použili v pracovním příkazu, nebude odpovídajícím způsobem aktualizována úroveň služby v požadavcích na údržbu a pracovních příkazech.
