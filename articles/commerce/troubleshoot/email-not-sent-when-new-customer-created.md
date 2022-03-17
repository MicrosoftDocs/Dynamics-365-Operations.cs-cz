---
title: Uvítací e-mail se neodesílá, když jsou vytvořeni noví zákazníci
description: Toto téma obsahuje pokyny pro odstraňování problémů, které vám mohou pomoci, pokud není při vytvoření nového zákazníka v Microsoft Dynamics 365 Commerce odeslán uvítací e-mailové upozornění.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349948"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Uvítací e-mail se neodesílá, když jsou vytvořeni noví zákazníci

[!include [banner](../../includes/banner.md)]

Toto téma obsahuje pokyny pro odstraňování problémů, které vám mohou pomoci, pokud není při vytvoření nového zákazníka v Microsoft Dynamics 365 Commerce odeslán uvítací e-mailové upozornění.

## <a name="description"></a>Popis

Když je vytvořen nový zákazník v ústředí Commerce, není zákazníkovi odeslán uvítací e-mail, i když je e-mailové upozornění nakonfigurováno pro typ upozornění e-mailem **Zákazník vytvořen**.

## <a name="resolution"></a>Řešení

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Nastavení správné hodnoty e-mailového ID pro typ upozornění vytvořený zákazník

Chcete-li nastavit správnou hodnotu **ID e-mailu** pro typ upozornění e-mailem **Zákazník vytvořen** v centrále, postupujte takto.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Profil upozornění e-mailem Commerce**.
1. V levém navigačním podokně vyberte profil upozornění e-mailem.
1. Pod **Nastavení oznámení o maloobchodních událostech** u typu upozornění e-mailem **Zákazník vytvořen** nastavte pole **ID e-mailu** na **NewCust**.

## <a name="additional-resources"></a>Další prostředky

[Nastavení profilu oznámení e-mailem](../email-notification-profiles.md)
