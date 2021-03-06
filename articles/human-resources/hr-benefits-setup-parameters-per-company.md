---
title: Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti
description: Nakonfigurujte parametry pro správu zaměstnaneckých výhod podle společnosti v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057615"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pro každou organizaci, která nabízí zaměstnanecké výhody, musíte nakonfigurovat nastavení e-mailů s potvrzením zaměstnaneckých výhod.

## <a name="configure-confirmation-email-settings"></a>Konfigurace nastavení e-mailu s potvrzením

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry lidských zdrojů**.

2. Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole: 

   | Pole | popis |
   | --- | --- |
   | **Odeslat e-mail s potvrzením** | Když je tato funkce zapnutá, bude zaměstnancům zaslán potvrzovací e-mail, když se registrují k zaměstnaneckým výhodám v samoobsluze pro zaměstnance. |
   | **E-mailová šablona pro potvrzení** | Vyberte šablonu e-mailu organizace, kterou chcete použít k odeslání potvrzení registrace. Pokud nevyberete šablonu, bude zaslán následující obecný e-mail:<br><br>%EmployeeFirstName%,<br><br>Gratulujeme! úspěšně jste se registrovali k zaměstnaneckým výhodám.<br><br>Děkujeme,<br>Zaměstnanecké výhody společnosti <název společnosti/organizace>. |
   | **Výchozí e-mailová adresa odesílatele** | E-mailová adresa, která se použije k odeslání potvrzovacího e-mailu. |

3. Zvolte **Uložit**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]