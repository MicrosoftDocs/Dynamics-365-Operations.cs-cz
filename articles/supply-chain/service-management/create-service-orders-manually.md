---
title: Ruční vytvoření servisních objednávek
description: Servisní zakázky můžete vytvářet ručně pomocí servisní smlouvy nebo pomocí formuláře **Servisní zakázky**.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51cfdb94a368df9e7082af3c768c79df44000342
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423840"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="a0ce4-103">Ruční vytvoření servisních objednávek</span><span class="sxs-lookup"><span data-stu-id="a0ce4-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a0ce4-104">Servisní zakázky můžete vytvářet ručně pomocí servisní smlouvy nebo pomocí formuláře **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="a0ce4-105">Servisní zakázku můžete také vytvořit z projektu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="a0ce4-106">Automatizované procesy slouží k vytváření servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="a0ce4-107">Ruční vytvoření servisní zakázky ze servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="a0ce4-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="a0ce4-108">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a0ce4-109">Vyberte servisní smlouvu nebo vytvořte novou servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="a0ce4-110">Klikněte na kartu **Dodávka** a ve skupině **Vytvořit** klikněte na **Plánované servisní zakázky** k otevření formuláře **Vytvořit servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="a0ce4-111">Ruční vytvoření servisní zakázky ve formuláři Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="a0ce4-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="a0ce4-112">Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a0ce4-113">Stisknutím kláves Ctrl+N vytvořte novou servisní zakázku.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="a0ce4-114">Vytvořte řádky servisní zakázky pro servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a0ce4-115">Jestliže je zaškrtnuto políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>Parametry servisní smlouvy</STRONG>, můžete transakce z řádků servisní zakázky účtovat bez připojení servisní zakázky k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a0ce4-116">Jestliže políčko není zaškrtnuto, je před zaúčtováním řádků servisní zakázky nutné připojit ručně vytvořenou servisní zakázku k projektu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="a0ce4-117">Vytvoření servisní zakázky z projektu</span><span class="sxs-lookup"><span data-stu-id="a0ce4-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="a0ce4-118">Klikněte na **Řízení a účetnictví projektů** \> **Společné** \> **Projekty** \> **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="a0ce4-119">Ve formuláři **Projekty** v **podokně akcí** klikněte na kartu **Správa** \> klikněte na **Servis** \> **Servisní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-119">In the **Projects** form, on the **Action Pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="a0ce4-120">Postupujte podle pokynů pro ruční vytvoření servisní zakázky ve formuláři **Servisní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="a0ce4-121">V poli **ID projektu** se zobrazuje reference na projekt.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a0ce4-122">Jestliže je zaškrtnuto políčko <STRONG>Povolit bez servisní smlouvy</STRONG> ve formuláři <STRONG>Parametry servisní smlouvy</STRONG>, můžete transakce z řádků servisní zakázky účtovat bez připojení servisní zakázky k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a0ce4-123">Jestliže políčko není zaškrtnuto, je před zaúčtováním řádků servisní zakázky nutné připojit ručně vytvořenou servisní zakázku k projektu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="a0ce4-124">Vytvoření servisních zakázek z formuláře Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="a0ce4-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="a0ce4-125">Servisní zakázku lze vytvořit z formuláře **Prodejní objednávky** pomocí průvodce **Vytvoření nové servisní zakázky na základě prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="a0ce4-126">Klikněte na **Prodej a marketing** \> **Společné** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="a0ce4-127">Otevřete příslušnou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="a0ce4-128">Na kartě **Prodejní objednávka** spusťte kliknutím na **Servisní zakázka** průvodce **Vytvoření nové servisní zakázky na základě prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="a0ce4-129">Klepněte na tlačítko **Další \>** a poté proveďte následující kroky na stránce **Vybrat smlouvu pro servisní zakázku**:</span><span class="sxs-lookup"><span data-stu-id="a0ce4-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="a0ce4-130">V poli **Servisní smlouva** vyberte servisní smlouvu, ke které by nová servisní zakázka měla být přidružena.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="a0ce4-131">(Volitelné): Použijte pole **ID projektu** pro přidružení servisní zakázky ke konkrétnímu projektu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="a0ce4-132">Klepněte na tlačítko **Další \>** a poté proveďte následující kroky na stránce **Vytvořit servisní zakázku**:</span><span class="sxs-lookup"><span data-stu-id="a0ce4-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="a0ce4-133">Do pole **Upřednostňovaný čas služby** zadejte datum a čas zahájení volání servisu.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="a0ce4-134">V případě potřeby text v poli **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="a0ce4-135">Ve výchozím nastavení obsahuje toto pole popis, který je popisem servisní smlouvy vybrané na předchozí stránce.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="a0ce4-136">V poli **Zodpovědná osoba** vyberte ID zaměstnance, který je odpovědný za smlouvu, a pokud znáte ID technika preferovaného odběratelem pro volání servisu, zadejte je.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="a0ce4-137">V poli **ID kontaktu** vyberte osobu ze společnosti odběratele, která by měla být v souvislosti s touto servisní zakázkou kontaktována.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="a0ce4-138">Klikněte na **Další \>** a potom na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="a0ce4-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="a0ce4-139">Viz také</span><span class="sxs-lookup"><span data-stu-id="a0ce4-139">See also</span></span>

[<span data-ttu-id="a0ce4-140">Servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="a0ce4-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="a0ce4-141">Automatické vytvoření servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="a0ce4-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="a0ce4-142">[Vytvoření servisních zakázek (formulář třídy)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a0ce4-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 

