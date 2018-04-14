---
title: "Konfigurace služby SQL Server Reporting Services pro místní nasazení"
description: "Toto téma obsahuje informace o konfiguraci služby SQL Server Reporting Services (SSRS) na místní nasazení."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bea198488da52de21aba0c33b4004b6ad7518fd3
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="c138b-103">Konfigurace služby SQL Server Reporting Services pro místní nasazení</span><span class="sxs-lookup"><span data-stu-id="c138b-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c138b-104">Kroky v tomto tématu lze použít ke konfiguraci služby SQL Server Reporting Services (SSRS) pro nasazení aplikace Microsoft Dynamics 365 for Finance and Operations, (on-premises).</span><span class="sxs-lookup"><span data-stu-id="c138b-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="c138b-105">Otevřete aplikaci Správce konfigurace služby Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="c138b-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="c138b-106">Ponechte výchozí **Název serveru**, což by měl být název aktuálního počítače, a **Instanci serveru sestav**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="c138b-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="c138b-107">Klepněte na tlačítko **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="c138b-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="c138b-108">[![Připojení konfigurace serveru sestav](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="c138b-109">Klepněte na **Účet služby** a ověřte, že parametry odpovídají následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c138b-110">[![Karta Účet služby](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="c138b-111">Klepněte na **Adresa URL webové služby** a ověřte, že parametry odpovídají následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="c138b-112">[![Karta Adresa URL webové služby](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="c138b-113">Klepněte na kartu **databáze** a ověřte, že **název databáze** a **pověření nastavení** odpovídají následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="c138b-114">**Poznámka:** Bude nutné vytvořit novou databázi.</span><span class="sxs-lookup"><span data-stu-id="c138b-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="c138b-115">Provedete to klepnutím na **změnit databázi** a ověřením, že nový název databáze je: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="c138b-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="c138b-116">[![karta databáze](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="c138b-117">Klepněte na **Adresa URL webového portálu** a ověřte, že parametry odpovídají následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="c138b-118">**Poznámka:** Vytvoření a správná konfigurace portálu vyžaduje, abyste klepli na tlačítko **Použít**.</span><span class="sxs-lookup"><span data-stu-id="c138b-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="c138b-119">[![karta Adresa url webového portálu](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
   <span data-ttu-id="c138b-120">Po nakonfigurování portálu bude karta **webový portál** odpovídat následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="c138b-121">[![karta webový portál](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="c138b-122">Klikněte na adresu URL sestav pro zobrazení webového portálu služby SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="c138b-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9. <span data-ttu-id="c138b-123">Až budete v portálu, můžete vytvořit novou složku pojmenovanou **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="c138b-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

   <span data-ttu-id="c138b-124">[![složka Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="c138b-125">Ve **Správci konfigurace služby Reporting Services** klepněte na **Nastavení e-mailu** a ověřte, že nastavení odpovídají následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c138b-126">[![karta nastavení e-mailu](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="c138b-127">Klepněte na **Účet spuštění** a ověřte, že parametry odpovídají následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c138b-128">[![karta účet provedení](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
    <span data-ttu-id="c138b-129">Neměňte výchozí nastavení na kartě **Šifrovací klíče**. [![karta šifrovacích klíčů](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="c138b-130">Klepněte na kartu **Nastavení předplatného** a ověřte, že parametry odpovídají následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c138b-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="c138b-131">[![karta nastavení předplatného](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
    <span data-ttu-id="c138b-132">Neměňte výchozí nastavení na kartě **Nasazení škálování**. [![karta nasazení škálování](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
    <span data-ttu-id="c138b-133">Neměňte výchozí nastavení na kartě **Integrace Power BI**. [![karta integrace Power BI](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="c138b-134">Kliknutím na tlačítko **Konec** zavřete **Správce konfigurace služby Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="c138b-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="c138b-135">[![zavření správce konfigurace služby reporting services](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="c138b-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


