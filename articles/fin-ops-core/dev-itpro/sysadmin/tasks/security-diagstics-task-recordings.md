---
title: Diagnostika zabezpečení pro záznamy úkolů
description: Tento článek poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb69bf997100f25cd0ad2b7e34139857199e5d00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880160"
---
# <a name="security-diagnostics-for-task-recordings"></a>Diagnostika zabezpečení pro záznamy úkolů

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Než začnete

Tento článek poskytuje informace o tom, jak analyzovat a spravovat požadavky na zabezpečení na základě záznamu úlohy. Než dokončíte kroky v tomto článku, musíte mít záznam úkolu obchodního procesu, který chcete analyzovat. Chcete-li zaznamenat obchodní proces, získáte informace v tématu [Zdroje záznamu úloh](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Správa zabezpečení záznamu úlohy

1. Přejděte na **Správa systému** > **Zabezpečení** > **Diagnostika zabezpečení pro záznam úlohy**.
2. Otevřete záznam úlohy z jeho umístění. Vyberte **Otevřít z tohoto počítače** nebo **Otevřít ze služby Lifecycle Services** a pak vyberte **Zavřít**.
3. Tím se otevře stránka **Podrobnosti položky nabídky zabezpečení**, která obsahuje seznam objektů zabezpečení požadovaných pro proces.

 > [!NOTE]
 > V seznamu nejsou uvedeny položky nabídky **Akce** a **Výstup**.

4. V poli **ID uživatele** vyberte uživatele. Pokud uživatel nemá oprávnění pro některé položky nabídky, pole **Chybějící oprávnění** se aktualizuje na **Ano**.
  
  ![Stránka podrobností položky nabídky zabezpečení.](../media/Security-Menu-Item-Details.png)

5. Vyberte **Přidat odkaz** pro zobrazení seznamu bezpečnostních objektů, včetně rolí, povinností a oprávnění, která udělují chybějící oprávnění.
6. Vyberte objekt zabezpečení ze seznamu.

    - Pokud je vybraná **Role**, vyberte **Přidat roli uživateli**. Otevře se stránka **Přiřadit uživatele rolím**. Další informace viz [Přiřazení uživatelů rolím zabezpečení](assign-users-security-roles.md).
    - Pokud je vybraná **Povinnost**, vyberte **Přiřadit povinnost roli**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.
    - Pokud je vybráno **Oprávnění**, vyberte **Přiřadit oprávnění povinnostem**, vyberte role, k nimž má být povinnost přidána, a vyberte **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]