---
title: Diagnostika zabezpečení pro záznamy úkolů
description: Toto téma poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679783"
---
# <a name="security-diagnostics-for-task-recordings"></a>Diagnostika zabezpečení pro záznamy úkolů

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Než začnete

Toto téma poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy. Než dokončíte kroky v tomto tématu, musíte mít záznam úkolu obchodního procesu, který chcete analyzovat. Chcete-li zaznamenat obchodní proces, získáte informace v tématu [Zdroje záznamu úloh](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Správa zabezpečení záznamu úlohy

1. Přejděte na **Správa systému** > **Zabezpečení** > **Diagnostika zabezpečení pro záznam úlohy**.
2. Otevřete záznam úlohy z jeho umístění. Vyberte **Otevřít z tohoto počítače** nebo **Otevřít ze služby Lifecycle Services** a pak vyberte **Zavřít**.
3. Tím se otevře stránka **Podrobnosti položky nabídky zabezpečení**, která obsahuje seznam objektů zabezpečení požadovaných pro proces.

 > [!NOTE]
 > V seznamu nejsou uvedeny položky nabídky **Akce** a **Výstup**.

4. V poli **ID uživatele** vyberte uživatele. Pokud uživatel nemá oprávnění pro některé položky nabídky, pole **Chybějící oprávnění** se aktualizuje na **Ano**.
  
  ![Stránka podrobností položky nabídky zabezpečení](../media/Security-Menu-Item-Details.png)

5. Vyberte **Přidat odkaz** pro zobrazení seznamu bezpečnostních objektů, včetně rolí, povinností a oprávnění, která udělují chybějící oprávnění.
6. Vyberte objekt zabezpečení ze seznamu.

    - Pokud je vybraná **Role**, vyberte **Přidat roli uživateli**. Otevře se stránka **Přiřadit uživatele rolím**. Další informace viz [Přiřazení uživatelů rolím zabezpečení](assign-users-security-roles.md).
    - Pokud je vybraná **Povinnost**, vyberte **Přiřadit povinnost roli**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.
    - Pokud je vybráno **Oprávnění**, vyberte **Přiřadit oprávnění povinnostem**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]