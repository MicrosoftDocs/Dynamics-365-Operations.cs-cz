---
title: "Konfigurace automatizované úlohy ve workflowu"
description: "Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 56e29bd2e875b8bb729e5dfe0c5ac03fc997ecbe
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a><span data-ttu-id="fcf39-103">Konfigurace automatizované úlohy ve workflowu</span><span class="sxs-lookup"><span data-stu-id="fcf39-103">Configure an automated task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fcf39-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="fcf39-105">Pokud budete chtít nakonfigurovat automatizovaný úkol v editoru workflowu, klikněte pravým tlačítkem myši na úkol a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="fcf39-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="fcf39-107">Pojmenování úlohy</span><span class="sxs-lookup"><span data-stu-id="fcf39-107">Name the task</span></span>
<span data-ttu-id="fcf39-108">Pomocí následujících kroků zadejte název automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-108">Follow these steps to enter a name for the automated task.</span></span>

1.  <span data-ttu-id="fcf39-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="fcf39-110">Do pole **Název** zadejte jedinečný název úlohy.</span><span class="sxs-lookup"><span data-stu-id="fcf39-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="fcf39-111">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="fcf39-111">Specify when notifications are sent</span></span>
<span data-ttu-id="fcf39-112">Lze odeslat oznámení uživatelům, kteří automatizovanou úlohu spustili nebo zrušili.</span><span class="sxs-lookup"><span data-stu-id="fcf39-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="fcf39-113">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="fcf39-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1.  <span data-ttu-id="fcf39-114">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-114">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="fcf39-115">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="fcf39-115">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="fcf39-116">**Spuštění** – oznámení jsou odeslána při spuštění úkolu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    -   <span data-ttu-id="fcf39-117">**Zrušení** – oznámení jsou odeslána při zrušení úkolu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3.  <span data-ttu-id="fcf39-118">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="fcf39-118">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="fcf39-119">Na kartě **Text oznámení** zadejte v textovém poli text oznámení.</span><span class="sxs-lookup"><span data-stu-id="fcf39-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="fcf39-120">Oznámení můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="fcf39-121">Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="fcf39-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="fcf39-122">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="fcf39-122">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="fcf39-123">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="fcf39-123">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="fcf39-124">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-124">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="fcf39-125">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="fcf39-125">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="fcf39-126">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-126">Click **Insert**.</span></span>

6.  <span data-ttu-id="fcf39-127">Chcete-li přidat překlady oznámení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="fcf39-127">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="fcf39-128">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-128">Click **Translations**.</span></span>
    2.  <span data-ttu-id="fcf39-129">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-129">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="fcf39-130">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="fcf39-131">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="fcf39-131">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="fcf39-132">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="fcf39-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="fcf39-133">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="fcf39-133">Click **Close**.</span></span>

7.  <span data-ttu-id="fcf39-134">Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána.</span><span class="sxs-lookup"><span data-stu-id="fcf39-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="fcf39-135">Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="fcf39-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="fcf39-136">Možnost</span><span class="sxs-lookup"><span data-stu-id="fcf39-136">Option</span></span></th>
    <th><span data-ttu-id="fcf39-137">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="fcf39-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="fcf39-138">Další kroky</span><span class="sxs-lookup"><span data-stu-id="fcf39-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="fcf39-139">Účastník</span><span class="sxs-lookup"><span data-stu-id="fcf39-139">Participant</span></span></td>
    <td><span data-ttu-id="fcf39-140">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="fcf39-140">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="fcf39-141">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="fcf39-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="fcf39-142">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="fcf39-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="fcf39-143">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="fcf39-143">Workflow user</span></span></td>
    <td><span data-ttu-id="fcf39-144">Uživatelé zúčastnění v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="fcf39-144">Users who participate in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="fcf39-145">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="fcf39-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="fcf39-146">Uživatel</span><span class="sxs-lookup"><span data-stu-id="fcf39-146">User</span></span></td>
    <td><span data-ttu-id="fcf39-147">Konkrétní uživatelé aplikace Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fcf39-147">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="fcf39-148">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="fcf39-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="fcf39-149">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fcf39-149">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="fcf39-150">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="fcf39-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="fcf39-151">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="fcf39-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>





