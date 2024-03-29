---
title: Konfigurace pracovníka s použitím mobilního pracovního zařízení
description: Tento článek popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844298"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurace pracovníka s použitím mobilního pracovního zařízení

[!include [banner](../../includes/banner.md)]

Tento článek popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Ověření, zda je pracovníkovi přiřazena určitá role

V tomto příkladu ověřte, zda je uživateli "SHANNON" přiřazena role operátora stroje před konfigurací účtu pracovníka.

1. Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.
2. Vyhledejte uživatele v rychlém filtru. V tomto příkladu zadejte `shannon`.
3. Vyberte odkaz ve sloupci **ID uživatele** uživatelského účtu, který se zobrazí.
4. Ve stromovém zobrazení **Uživatelské role** vyberte **Role > Operátor stroje**.
5. Zavřete **Podrobnosti uživatele** a stránky **uživatelů** a vraťte se na domovskou stránku.

## <a name="configure-worker-account"></a>Nastavte konfiguraci účtu pracovníka
1. Přejděte na **Navigační podokno > Moduly > Lidské zdroje > Pracovníci > Pracovníci**.
2. Vyhledejte uživatele v rychlém filtru. V tomto příkladu zadejte `shannon`.
3. Vyberte odkaz ve sloupci **Název** uživatelského účtu, který se zobrazí.
4. Vyberte záložku **Registrace času**.
5. Vyberte **Aktivovat na terminálech registrace**.
6. V následujících polích zadejte hodnoty:  

    - **Skupina výpočtu**  
    - **Výchozí skupina výpočtu**  
    - **Skupina schválení**  
    - **Standardní profil**  
    - **Skupina profilu**  

7. Vyberte **OK**.
8. Vyberte tlačítko **Upravit** zadejte číslo znaku pro novou registraci pracovníka. V poli **ID znaku** zadejte hodnotu.
9. Zvolte **Uložit**.
10. Zavřete stránky **Podrobnosti o pracovníkovi** a **Pracovníci**.

## <a name="assign-worker-to-device-group"></a>Přiřaďte pracovníka ke skupině zařízení
1. Přejděte do nabídky **Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení**.
2. Vyberte **přidat**.
3. Vyberte požadovaného pracovníka v seznamu. V tomto příkladu vyberte **SHANNON**.
4. Vyberte **OK**.
5. Vyberte možnost **Upravit**.
6. V poli **Výrobní jednotka** lze nastavit výchozí filtr pro pracovníka. Tím bude zajištěno, že pouze výrobní práce pro vybrané výrobní jednotky se zobrazí v případě, že se pracovník přihlásí k zařízení. Zadejte požadovanou hodnotu.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]