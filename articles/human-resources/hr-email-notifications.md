---
title: E-mailové upozornění na zaměstnanecké výhody
description: Tento článek poskytuje přehled funkce e-mailových oznámení správy zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229895"
---
# <a name="benefits-email-notification"></a>E-mailové upozornění na zaměstnanecké výhody

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Funkce upozornění e-mailem umožňuje zasílání upozornění a připomenutí e-mailem zaměstnancům v následujících situacích:

- Registrace nového zaměstnance
- Otevřená registrace
- Kvalifikující životní události

Můžete vytvořit a nastavit více e-mailových šablon a odeslat upozornění pomocí pracovního prostoru **Správa zaměstnaneckých výhod** a stránky **Zaměstnanecké výhody**. Můžete také sledovat historii upozornění/připomenutí.

## <a name="set-up-human-resources-shared-parameters"></a>Nastavení sdílených parametrů lidských zdrojů

Na stránce **Sdílené parametry lidských zdrojů** můžete vytvořit šablony e-mailů se zaměstnaneckými výhodami pro různé typy komunikace, které jsou zasílány zaměstnancům nebo skupinám zaměstnanců.

## <a name="create-a-new-email-id-template"></a>Vytvoření nové šablony ID e-mailu

Novou šablonu ID e-mailu vytvoříte takto:

1. Přejděte na **Šablony e-mailu systému**.
2. Zvolte **Nové**.
3. Do pole **ID e-mailu** zadejte název.
4. V případě potřeby nastavte další pole.
5. Vyberte **E-mailová zpráva** k nahrání šablony.
6. Na stránce **Sdílené parametry lidských zdrojů** vyberte novou šablonu pod **Systémové šablony** a přesuňte ji pod **Šablony pro zaměstnanecké výhody**.

## <a name="send-email-to-employees"></a>Odeslání e-mailu zaměstnancům

Chcete-li poslat e-mail nově přijatému zaměstnanci, který ještě nezačal, postupujte takto.

1. Otevřete pracovní prostor **Správa zaměstnaneckých výhod**.
2. Vyberte dlaždici pro skupinu zaměstnanců, kterým chcete poslat e-mail.
3. Vyberte **Odeslat e-mail**.
4. Vyberte zaměstnance, kterým chcete poslat e-mail.
5. Vyberte **Odeslat e-mail**.
6. Vyberte šablonu, kterou chcete použít.
7. Výběrem **OK** odešlete e-mail.

    E-mailovou zprávu a stav si můžete prohlédnout na stránce **Zaměstnanecké výhody** zaměstnanec nebo výběrem **Historie e-mailů se zaměstnaneckými výhodami** v části **Odkazy** pracovního prostoru **Správa zaměstnaneckých výhod**. E-mail můžete také odeslat ze stránky **Plán zaměstnaneckých výhod**.

8. Chcete-li zobrazit historii e-mailů zaměstnaneckých výhod, v pracovním prostoru **Správa zaměstnaneckých výhod** v části **Odkazy** vyberte **Historie e-mailů se zaměstnaneckými výhodami**.
9. Prohlédněte si kompletní e-mailovou historii odeslaných e-mailů se zaměstnaneckými výhodami. Chcete-li zkontrolovat obsah e-mailu, vyberte **Zobrazit zprávu**.
10. Vyberte **Pracovník**.
11. Na stránce **Plán zaměstnaneckých výhod pracovníka** můžete odeslat e-mail a zobrazit historii e-mailů se zaměstnaneckými výhodami.

Pracovní prostor **Správa zaměstnaneckých výhod** obsahuje různé dlaždice. E-maily můžete odesílat výběrem související šablony. Pokud byly odeslány e-maily s registrací nově přijatého zaměstnance, vyberte možnost **Nově přijatý zaměstnanec ještě nezačal** a poté vyberte odkaz **Odeslat připomínku**. Můžete vybrat šablonu připomenutí a nastavit název oznámení jako první, druhé nebo třetí připomenutí.
