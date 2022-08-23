---
title: Uvítací e-mail se neodesílá, když jsou vytvořeni noví zákazníci
description: Tento článek obsahuje pokyny pro odstraňování problémů, které vám mohou pomoci, pokud není při vytvoření nového zákazníka v Microsoft Dynamics 365 Commerce odeslán uvítací e-mailové upozornění.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219397"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Uvítací e-mail se neodesílá, když jsou vytvořeni noví zákazníci

[!include [banner](../../includes/banner.md)]

Tento článek obsahuje pokyny pro odstraňování problémů, které vám mohou pomoci, pokud není při vytvoření nového zákazníka v Microsoft Dynamics 365 Commerce odeslán uvítací e-mailové upozornění.

## <a name="description"></a>Popis

Když je vytvořen nový zákazník v ústředí Commerce, není zákazníkovi odeslán uvítací e-mail, i když je e-mailové upozornění nakonfigurováno pro typ upozornění e-mailem **Zákazník vytvořen**.

## <a name="resolution"></a>Řešení

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Přidružení profilu e-mailových upozornění pod parametry Commerce

1. V aplikaci Headquarters přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry aplikace Commerce \> Obecné**.
2. V rozevíracím seznamu **Profil e-mailových upozornění** vyberte profil upozornění e-mailem, který obsahuje mapování mezi typem upozornění vytvořeným zákazníkem a e-mailovou šablonou vytvořenou zákazníkem.  

> [!NOTE] 
> Když aktivujete oznámení vytvořená zákazníkem, zákazníci, kteří jsou vytvořeni ve všech kanálech v rámci právnické osoby, obdrží e-mail vytvořený zákazníkem. V současné době nelze oznámení vytvořená zákazníkem omezit na jeden kanál.

Další informace viz [Vytvoření e-mailových šablon pro transakční události](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Další prostředky

[Nastavení profilu oznámení e-mailem](../email-notification-profiles.md)
