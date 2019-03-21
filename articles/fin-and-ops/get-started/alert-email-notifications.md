---
title: Výstražná upozornění klientovi e-mailem
description: Toto téma obsahuje informace o nastavení pravidel, která budou odesílat e-mailová oznámení, pokud dojde k předem definované události.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: a13f44549ab402cfd04b600f6097ba179915f233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "775057"
---
# <a name="client-alert-notifications-by-email"></a>Výstražná upozornění klientovi e-mailem

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

V aplikaci Microsoft Dynamics 365 for Finance and Operations můžete definovat vlastní pravidla výstrah, která sledují filtrovaná zobrazení dat a automaticky odesílají oznámení e-mailem, když dojde k předem definované události. Možnost odeslání e-mailového oznámení je k dispozici pro všechny podporované typy výstrah a lze ji rovněž zapnout pro existující pravidla výstrah.

Můžete použít vestavěné ovládací prvky k vytváření pravidel výstrah, která sledují filtrovaná zobrazení dávkových úloh systému. Sledováním hodnoty pole **Stav** můžete také nastavit pravidla výstrah, která odesílají e-mail při selhání dávkové úlohy. Po vytvoření těchto pravidel výstrah již nemusíte kontrolovat sestavy ohledně změn obchodní dat. Místo toho můžete nechat inteligentní službu detekce změny Finance and Operations, aby prováděla monitoring za vás.

Výstrahy klienta závisí na podsystému e-mailu, který je poskytován prostřednictvím integrace s Microsoft Office. Doporučujeme použít poskytovatele SMTP, aby e-mailová distribuce nemusela spoléhat na lokálního e-mailového klienta.

Aby mohli odesílat oznámení e-mailem, musí odběratelé nakonfigurovat integrované e-mailové služby. E-mailová oznámení se odesílají příjemcům jménem vlastníků výstrahy.

Další informace o způsobu konfigurace e-mailu v aplikaci Finance and Operations naleznete v tématu [Konfigurace a odesílání e-mailu](../organization-administration/configure-email.md).

Následující obrázek znázorňuje dialogové okno **Vytvoření pravidla výstrahy**, které nyní zahrnuje možnost **Odeslat e-mail**.

[![Dialogové okno vytvoření pravidla výstrahy, kde je možnost Odeslat e-mail nastavena na Ano](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Když je možnost **Odeslat e-mail** nastavena na **Ano**, výstražná oznámení budou nadále doručována z Centra akcí.

## <a name="alert-notification-email-templates"></a>Šablony e-mailu s výstražným upozorněním

Služba odešle e-mailová upozornění pomocí předdefinovaných šablon e-mailu, které doručují základní podrobnosti výstražných upozornění.

Následující obrázek zobrazuje strukturu výstražných oznámení při přijetí e-mailem.

[![Výstražná upozornění založená na šabloně pro vytvoření záznamu, změny polí a odstranění šablon](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
