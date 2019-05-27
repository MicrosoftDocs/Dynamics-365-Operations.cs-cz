---
title: Konfigurace pracovníka s použitím mobilního pracovního zařízení
description: Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571351"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurace pracovníka s použitím mobilního pracovního zařízení

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.


## <a name="assign-roles-to-user-account"></a>Přiřadit role uživatelskému účtu
1. Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.
2. Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje. V ukázkových datech by toto jméno bylo Shannon.
3. Vyberte záznam uživatelského účtu.
4. V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.
5. Ve stromovém zobrazení vyberte „Role\Operátor stroje“.
6. Zavřete stránku s podrobnostmi o uživatelském účtu.
7. Zavřete stránku.

## <a name="configure-worker-account"></a>Nastavte konfiguraci účtu pracovníka.
1. Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.
2. Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje. V ukázkových datech by toto jméno bylo Shannon.
3. Vyberte záznam uživatelského účtu.
4. V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.
5. Klikněte na kartu Zaměstnání.
6. Rozbalte pevnou záložku Registrace času a klikněte na tlačítko Aktivovat na terminálech registrace.
7. Klikněte na terminálech registrace na Aktivovat.
8. V poli Skupina výpočtu zadejte nebo vyberte hodnotu.
9. V poli Výchozí skupina výpočtu zadejte nebo vyberte hodnotu.
10. V poli Skupina schválení zadejte nebo vyberte hodnotu.
11. V poli Standardní profil zadejte nebo vyberte hodnotu.
12. V poli Skupina profilu zadejte nebo vyberte hodnotu.
13. Klepněte na tlačítko OK.
14. Kliknutím na tlačítko Upravit zadejte číslo znaku pro novou registraci pracovníka.
15. Zadejte hodnotu do pole ID znaku.
16. Klepněte na tlačítko Uložit.
17. Použijte zástupce SaveRecord.
18. Zavřete stránku s podrobnostmi o pracovníkovi.
19. Zavřete stránku.

## <a name="assign-worker-to-device-group"></a>Přiřaďte pracovníka ke skupině zařízení.
1. Přejděte do nabídky Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení.
2. Klepněte na možnost Přidat.
3. Označte v seznamu vybraný řádek.
4. Klikněte na tlačítko OK.
5. Klikněte na položku Upravit.
6. V poli Výrobní jednotka lze nastavit výchozí filtr pro pracovníka. Tím bude zajištěno, že pouze výrobní práce pro vybrané výrobní jednotky se zobrazí v případě, že se pracovník přihlásí k zařízení.
7. Zavřete stránku.

