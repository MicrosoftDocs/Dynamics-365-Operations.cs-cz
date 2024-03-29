---
title: Úrovně služeb majetku
description: V tomto článku jsou vysvětleny úrovně služby Majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908678"
---
# <a name="asset-service-levels"></a>Úrovně služeb majetku

[!include [banner](../../includes/banner.md)]

 

V tomto článku jsou vysvětleny úrovně služby Majetek v modulu Správa majetku. Úrovně služby Majetek jsou spojeny s majetkem a jsou převedeny do požadavků na údržbu a pracovních příkazů. Používají se k výpočtu priority pracovních příkazů během plánování pracovních příkazů. Úrovně služby majetek lze změnit, pokud jsou požadovány změny.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]