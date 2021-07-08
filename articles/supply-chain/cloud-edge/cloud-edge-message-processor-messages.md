---
title: Zprávy procesoru zpráv
description: Toto téma poskytuje informace o funkci zpráv procesoru zpráv pro úlohy jednotky škálování.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 86f15831f11dc9fdcada9639858fd3b18cdc7503
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271094"
---
# <a name="message-processor-messages"></a><span data-ttu-id="0ae7f-103">Zprávy procesoru zpráv</span><span class="sxs-lookup"><span data-stu-id="0ae7f-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ae7f-104">Zprávy procesoru zpráv se používají při spuštění cloudových a hranových jednotek pro [výrobní úlohy](cloud-edge-workload-manufacturing.md) a [úlohy správy skladu](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="0ae7f-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="0ae7f-105">Mezi prostředím nasazení centra a jednotky škálování se vyměňuje velké množství dat, aby byla synchronizována, ale pouze několik z těchto výměn dat bude zpracováno *procesorem zpráv*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="0ae7f-106">Zprávy zpracované procesorem zpráv můžete zobrazit přechodem na **Správa systému >Procesor zpráv > Zprávy procesoru zpráv**.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="0ae7f-107">Sloupce a filtry mřížky zpráv</span><span class="sxs-lookup"><span data-stu-id="0ae7f-107">Message grid columns and filters</span></span>

<span data-ttu-id="0ae7f-108">Můžete použít pole v horní části stránky **Zprávy procesoru zpráv** k nalezení konkrétních zpráv, které hledáte.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="0ae7f-109">Většina z těchto filtrů odpovídá záhlaví sloupců v mřížce zpráv.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="0ae7f-110">K dispozici jsou následující filtry a záhlaví sloupců:</span><span class="sxs-lookup"><span data-stu-id="0ae7f-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="0ae7f-111">**Typ zprávy** – Určuje typ zprávy.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="0ae7f-112">**Fronta zpráv** – Určuje název fronty, ve které má být zpráva zpracována.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="0ae7f-113">K dispozici jsou následující fronty:</span><span class="sxs-lookup"><span data-stu-id="0ae7f-113">The following queues are provided:</span></span>
  - <span data-ttu-id="0ae7f-114">*Jednotka škálování na centrum*</span><span class="sxs-lookup"><span data-stu-id="0ae7f-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="0ae7f-115">*Centrální uzel na jednotku škálování provádění skladu*</span><span class="sxs-lookup"><span data-stu-id="0ae7f-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="0ae7f-116">*Centrální uzel na jednotku škálování provádění výroby*</span><span class="sxs-lookup"><span data-stu-id="0ae7f-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="0ae7f-117">**Stav zprávy** – Určuje stav zprávy.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="0ae7f-118">K dispozici jsou následující stavy:</span><span class="sxs-lookup"><span data-stu-id="0ae7f-118">The following states exists:</span></span>
  - <span data-ttu-id="0ae7f-119">*Ve frontě* – Zpráva je připravena ke zpracování procesorem zpráv.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="0ae7f-120">*Zpracováno* – Zpráva byla úspěšně zpracována procesorem zpráv.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="0ae7f-121">*Zrušeno* – Zpráva byla zpracována, ale zpracování se nezdařilo.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="0ae7f-122">**Obsah zprávy** – Tento filtr provádí fulltextové vyhledávání obsahu zprávy.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="0ae7f-123">(Obsah zprávy se v mřížce nezobrazuje.) Filtr považuje většinu speciálních symbolů (například „-“) za mezery a všechny znaky mezery za logické operátory OR.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="0ae7f-124">T=Například toto znamená, pokud hledáte konkrétní hodnotu `journalid` rovnou „USMF-123456“, že systém najde všechny zprávy, které obsahují „USMF“ nebo „123456“, což bude pravděpodobně dlouhý seznam.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="0ae7f-125">Proto by bylo lepší zadat pouze „123456“ samostatně, protože to vrátí konkrétnější výsledky.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="0ae7f-126">Příklad typu zprávy: Žádost o finanční aktualizaci zásob</span><span class="sxs-lookup"><span data-stu-id="0ae7f-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="0ae7f-127">Například **Typ zprávy** *Vyžádat finanční aktualizaci zásob* se používá k vytvoření a zaúčtování deníku počítání na centru, když pracovník používá aplikaci skladu k [registraci úpravy zásob](cloud-edge-warehouse-inventory-adjustment.md) na úloze správy skladu jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="0ae7f-128">Protože tento konkrétní proces pochází z jednotky škálování, pole **Fronta zpráv** zobrazí hodnotu *Jednotka škálování na centrum*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="0ae7f-129">U tohoto typu zprávy úloha jednotky škálování zaznamenává zprávu jako součást operace úpravy zásob aplikace skladu.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="0ae7f-130">Data zprávy se poté přenesou do centra jako součást stejného procesu, jaký se používá pro [architekturu Commerce Data Exchange](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="0ae7f-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="0ae7f-131">Zpráva bude aktualizována, aby se zobrazila **Stav zprávy** jako *Ve frontě*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="0ae7f-132">Procesor zprávy se poté pokusí zprávu zpracovat a aktualizuje **Stav zprávy** na *Zpracováno* při úspěchu nebo *Zrušeno* při selhání.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="0ae7f-133">Zobrazit protokol zpráv, obsah zprávy a podrobnosti</span><span class="sxs-lookup"><span data-stu-id="0ae7f-133">View the message log, message content, and details</span></span>

<span data-ttu-id="0ae7f-134">Podrobné informace o zprávě najdete tak, že ji vyberete v mřížce a poté otevřete karty **Protokol** nebo **Obsah zprávy** pod mřížkou zpráv, kde se zobrazuje každá událost zpracování.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="0ae7f-135">**Obsah zprávy** závisí na **Typ zprávy**, a proto budou mít jinou délku textu.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="0ae7f-136">Typický text obsahu zprávy začíná **{** a končí **}** a mezitím mají názvy polí jako `journalId` následovaný **:** a hodnotu, jako je *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="0ae7f-137">Panel nástrojů na kartě **Protokol** obsahuje následující tlačítka:</span><span class="sxs-lookup"><span data-stu-id="0ae7f-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="0ae7f-138">**Protokol** – Zobrazí výsledky zpracování.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="0ae7f-139">To je zvláště užitečné pro pochopení důvodů selhání zpracování zpráv, které mají **Výsledek zpracování** *Selhalo*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="0ae7f-140">**Balíček** – Více operací zpracování zpráv lze spustit jako součást stejného dávkového procesu.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="0ae7f-141">Toto tlačítko vyberte, chcete-li zobrazit tato podrobná data.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="0ae7f-142">Například můžete zjistit, zda existují závislosti, které vyžadují, aby systém zpracovával určité zprávy v konkrétním pořadí.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="0ae7f-143">Dávková úloha procesoru zpráv</span><span class="sxs-lookup"><span data-stu-id="0ae7f-143">Message processor batch job</span></span>

<span data-ttu-id="0ae7f-144">Při spuštění cloudového a hranového nasazení dávková úloh *Procesor zpráv* bude automaticky vyvolána, když je vytvořena nová zpráva ke zpracování, abyste tuto úlohu nemuseli plánovat ručně.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="0ae7f-145">V případě potřeby můžete k dávkové úloze přejít na **Správa systému > Procesor zpráv > Procesor zpráv**.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="0ae7f-146">Ruční zpracování nebo zrušení zprávy</span><span class="sxs-lookup"><span data-stu-id="0ae7f-146">Manually process or cancel a message</span></span>

<span data-ttu-id="0ae7f-147">V případě potřeby můžete zprávu ručně zpracovat nebo zrušit v závislosti na jejím aktuálním stavu.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="0ae7f-148">Chcete-li tak učinit, vyberte zprávu v mřížce a poté vyberte **Proces** nebo **Zrušit** v podokně Akce</span><span class="sxs-lookup"><span data-stu-id="0ae7f-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="0ae7f-149">Nastavte obchodní události k doručování upozornění na neúspěšné výsledky zpracování</span><span class="sxs-lookup"><span data-stu-id="0ae7f-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="0ae7f-150">Kromě filtrování na hodnotu **Stav zprávy** *Zrušeno*, chcete-li zjistit neúspěšné zprávy, můžete nastavit [Obchodní akce](../../fin-ops-core/dev-itpro/business-events/home-page.md) na centru, aby vás upozornily na neúspěšné výsledky zpracování.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="0ae7f-151">Chcete-li tak učinit, aktivujte obchodní událost s názvem *Zpráva procesoru zprávy byla zpracována* na stránce **Katalog obchodních akcí** (**Správa systému > Nastavení > Obchodní události > Katalog obchodních událostí**).</span><span class="sxs-lookup"><span data-stu-id="0ae7f-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="0ae7f-152">V rámci aktivačního procesu budete vedeni k určení, zda je událost specifická pro jeden nebo všechny právnické osoby, a uvedete **Název koncového bodu**, který musí být definován jako první.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="0ae7f-153">Poku je **Když dojde k obchodní události** nastaveno na *Microsoft Power Automate* (a ne například *HTTPS*), **Název koncového bodu** bude automaticky vytvořen v Supply Chain Management na základě nastavení *Microsoft Power Automate*.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="0ae7f-154">Příklad Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="0ae7f-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="0ae7f-155">V tomto příkladu použijte **Když dojde k obchodní události** s *Microsoft Power Automate*, který posílá e-maily obsahující zprávy InfoLog a hypertextové odkazy k otevření stránky **Zprávy procesoru zpráv** pro konkrétní neúspěšnou zprávu o nasazení centra.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="0ae7f-156">V případě potřeby můžete přidat další logiku pro paralelní odesílání oznámení pomocí různých kanálů a kontrolu příjemců na základě dat události.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="0ae7f-157">V [Power Automate](https://preview.flow.microsoft.com) vytvořte nový automatizovaný cloudový tok pro aktivační událost toku **Když dojde k obchodní události – aplikace Fin & Ops (Dynamics 365)** následovaný kroky **Analyzovat JSON** a **Poslat email**, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Automatizovaný cloudový tok Power Automate":::

1. <span data-ttu-id="0ae7f-159">V kroku **Když dojde k obchodní události** můžete vyhledat nebo zadat **Instance** centra po **Kategorie** a pak **Obchodní akce** *Zpráva procesoru zprávy byla zpracována*, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Krok, když dojde k obchodní události":::

1. <span data-ttu-id="0ae7f-161">Pro krok **Analyzovat JSON** zadejte **Schéma**, které definuje rozšířená pole.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="0ae7f-162">Můžete použít možnost *Stáhnout schéma* na stránce **Katalog obchodních akcí** v Supply Chain Management nebo začněte vložením příkladu textu schématu.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="0ae7f-163">Tento příklad textu je uveden za následujícím obrázkem.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Analyzovat krok JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="0ae7f-165">V kroku **Poslat email** můžete vybrat jednotlivá pole nebo začít vložením příkladu těla e-mailu do pole **Tělo**.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="0ae7f-166">Tento příklad je uveden za následujícím obrázkem.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate – krok odeslání zprávy":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="0ae7f-168">Když obchodní událost uložíte, bude automaticky aktivována a připravena k použití jako součást Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0ae7f-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
