---
title: Tisk platby DPH podle sestavy kódu
description: Toto téma obsahuje informace o nastavení a akcích, které jsou nutné k vytištění platby DPH podle kódu v měně účtování nebo kódu DPH.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 7c863308d2efc442ad16973407fe1cb72fb68cf89204c20f4468a3c98f4740c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774322"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Tisk platby DPH podle sestavy kódu 

[!include [banner](../includes/banner.md)]

Chcete-li vytisknout **platbu DPH podle kódu**, přejděte na **Daně** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platba DPH podle kódu**. Ve výchozím nastavení jsou částky sestavy generovány v zúčtovací měně právnické osoby pro všechny kódy vykazování, které jsou nastaveny na stránce **Kódy vykazování DPH**.

Tuto sestavu lze rovněž vygenerovat tak, aby v měnách kódů DPH pro všechny kódy vykazování přiřazené ke kódům DPH na stránce **kódy DPH** byla zobrazena částka platby DPH.

## <a name="turn-on-the-feature"></a>Zapnutí funkce

V pracovním prostoru **Správa funkcí** zapněte následující funkci: **Generovat sestavu plateb DPH podle kódu v měně kódu DPH**.

## <a name="run-the-report"></a>Spuštění sestavy 

1. Přejděte na **Daň** \> **Dotazy a sestavy** \> **Sestavy DPH** \> **Platby DPH dle kódu**.
2. V poli **Měna sestavy** vyberte některou z následujících hodnot:

    - **Zúčtovací měna** – tisk částek sestavy v zúčtovací měně.
    - **Měna kódu DPH** – Tisk částek sestavy v měnách kódů DPH.

    ![Dialogové okno Platba DPH dle kódu (sestava).](media/Sales-tax-payment-by-code.png)

Následující obrázek znázorňuje příklad vygenerované sestavy. Sestava ukazuje, že kód vykazování **101** má měnu **EUR**, pokud je pole **Měna DPH** nastaveno na **EUR** pro kód DPH, ke kterému je kód vykazování přiřazen.

![Příkald sestavy Platba DPH podle kódu.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]