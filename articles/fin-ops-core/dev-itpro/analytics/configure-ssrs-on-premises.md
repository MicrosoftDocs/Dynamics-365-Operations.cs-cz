---
title: Konfigurace služby SQL Server Reporting Services pro místní nasazení
description: Toto téma obsahuje informace o konfiguraci služby SQL Server Reporting Services (SSRS) na místní nasazení.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174229"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>Konfigurace služby SQL Server Reporting Services pro místní nasazení

[!include [banner](../includes/banner.md)]

Postupujte podle kroků v tomto tématu pro konfiguraci služby SQL Server Reporting Services pro vaše nasazení Microsoft Dynamics 365 Finance + Operations (on-premises).

1. Otevřete aplikaci Správce konfigurace služby Reporting Services.
2. Ponechte výchozí **Název serveru**, což by měl být název aktuálního počítače, a **Instanci serveru sestav**, **MSSQLSERVER**.
3. Klepněte na tlačítko **Připojit**.

    [![Připojení konfigurace serveru sestav](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klepněte na **Účet služby** a ověřte, že parametry odpovídají následujícím obrázku.

    [![Karta Účet služby](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klepněte na **Adresa URL webové služby** a ověřte, že parametry odpovídají následujícím obrázku.

    [![Karta Adresa URL webové služby](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klepněte na kartu **databáze** a ověřte, že **název databáze** a **pověření nastavení** odpovídají následujícímu obrázku.

    > [!NOTE]
    > Bude nutné vytvořit novou databázi. Provedete to klepnutím na **změnit databázi** a ověřením, že nový název databáze je: **DynamicsAxReportServer**.

    [![karta databáze](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klepněte na **Adresa URL webového portálu** a ověřte, že parametry odpovídají následujícímu obrázku.

    > [!NOTE]
    > Vytvoření a správná konfigurace portálu vyžaduje, abyste klepli na tlačítko **Použít**.

    [![karta Adresa url webového portálu](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Po nakonfigurování portálu bude karta **webový portál** odpovídat následujícímu obrázku.

    [![karta webový portál](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klikněte na adresu URL sestav pro zobrazení webového portálu služby SQL Server Reporting Services.
9. Až budete v portálu, můžete vytvořit novou složku pojmenovanou **Dynamics**.

    [![složka Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Ve **Správci konfigurace služby Reporting Services** klepněte na **Nastavení e-mailu** a ověřte, že nastavení odpovídají následujícímu obrázku.

    [![karta nastavení e-mailu](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klepněte na **Účet spuštění** a ověřte, že parametry odpovídají následujícímu obrázku.

    [![karta účet provedení](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Neměňte výchozí nastavení na kartě **Šifrovací klíč**.

    [![karta šifrovací klíče](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klepněte na kartu **Nastavení předplatného** a ověřte, že parametry odpovídají následujícímu obrázku.

    [![karta nastavení předplatného](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Neměňte výchozí nastavení na kartě **Nasazení škálování**.

    [![karta nasazení škálování](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Neměňte výchozí nastavení na kartě **Integrace Power BI**.

    [![karta integrace power bi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Kliknutím na tlačítko **Konec** zavřete **Správce konfigurace služby Reporting Services**.

    [![zavření správce konfigurace služby reporting services](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
