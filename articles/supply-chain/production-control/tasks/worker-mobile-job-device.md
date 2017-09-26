--- 
title: "Konfigurace pracovníka s použitím mobilního pracovního zařízení"
description: "Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7da224809946d90387668d25c5aed5b61f6a7b72
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Konfigurace pracovníka s použitím mobilního pracovního zařízení

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


