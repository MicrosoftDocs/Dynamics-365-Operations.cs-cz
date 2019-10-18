---
title: Konfigurace automatizovaných úloh ve workflowu
description: Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c02b4ff61b5b1f1e69d7fc0d537fe5ce535a430
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190228"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="ffe00-103">Konfigurace automatizovaných úloh ve workflowu</span><span class="sxs-lookup"><span data-stu-id="ffe00-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffe00-104">Toto téma vysvětluje, jak nakonfigurovat vlastnosti automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="ffe00-105">Pokud budete chtít nakonfigurovat automatizovaný úkol v editoru workflowu, klikněte pravým tlačítkem myši na úkol a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ffe00-106">Následně nakonfigurujte vlastnosti dílčího workflowu pomocí automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="ffe00-107">Pojmenování úlohy</span><span class="sxs-lookup"><span data-stu-id="ffe00-107">Name the task</span></span>

<span data-ttu-id="ffe00-108">Pomocí následujících kroků zadejte název automatizovaného úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="ffe00-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ffe00-110">Do pole **Název** zadejte jedinečný název úlohy.</span><span class="sxs-lookup"><span data-stu-id="ffe00-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ffe00-111">Zadejte, kdy se mají odesílat oznámení.</span><span class="sxs-lookup"><span data-stu-id="ffe00-111">Specify when notifications are sent</span></span>

<span data-ttu-id="ffe00-112">Lze odeslat oznámení uživatelům, kteří automatizovanou úlohu spustili nebo zrušili.</span><span class="sxs-lookup"><span data-stu-id="ffe00-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="ffe00-113">Podle těchto kroků můžete určit oznámení, které se odešle, a osoby, kterým se odešle.</span><span class="sxs-lookup"><span data-stu-id="ffe00-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="ffe00-114">V levém podokně klikněte na **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ffe00-115">Označte pole vedle událostí, při kterých se oznámení odešle:</span><span class="sxs-lookup"><span data-stu-id="ffe00-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="ffe00-116">**Spuštění** – oznámení jsou odeslána při spuštění úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="ffe00-117">**Zrušení** – oznámení jsou odeslána při zrušení úkolu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="ffe00-118">Vyberte řádek pro událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="ffe00-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ffe00-119">Na kartě **Text oznámení** zadejte v textovém poli text oznámení.</span><span class="sxs-lookup"><span data-stu-id="ffe00-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="ffe00-120">Oznámení můžete přizpůsobit vložením zástupného textu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="ffe00-121">Zástupný text bude při zobrazení oznámení uživatelům nahrazen odpovídacími daty.</span><span class="sxs-lookup"><span data-stu-id="ffe00-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="ffe00-122">Při vkládání zástupného textu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffe00-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ffe00-123">V textovém poli klepnutím zadejte, kde se má zástupný text zobrazit.</span><span class="sxs-lookup"><span data-stu-id="ffe00-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ffe00-124">Klikněte na **Vložit zástupný text**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ffe00-125">V nově otevřeném seznamu vyberte vkládaný zástupný text.</span><span class="sxs-lookup"><span data-stu-id="ffe00-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ffe00-126">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-126">Click **Insert**.</span></span>

6. <span data-ttu-id="ffe00-127">Chcete-li přidat překlady oznámení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="ffe00-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="ffe00-128">Klikněte na **Překlady**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="ffe00-129">Na nově otevřené stránce klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ffe00-130">V nově otevřeném seznamu vyberte jazyk, který chcete použít pro zadání textu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ffe00-131">V poli **Přeložený text** zadejte text.</span><span class="sxs-lookup"><span data-stu-id="ffe00-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ffe00-132">Text můžete přizpůsobit vložením zástupného textu podle pokynů v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="ffe00-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="ffe00-133">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="ffe00-133">Click **Close**.</span></span>

7. <span data-ttu-id="ffe00-134">Na kartě **Příjemce** zadejte osoby, kterým budou upozornění odesílána.</span><span class="sxs-lookup"><span data-stu-id="ffe00-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="ffe00-135">Vyberte jednu z možností v následující tabulce a před přechodem na krok 8 postupujte podle dalších kroků pro tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="ffe00-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ffe00-136">Možnost</span><span class="sxs-lookup"><span data-stu-id="ffe00-136">Option</span></span></th>
    <th><span data-ttu-id="ffe00-137">Příjemce oznámení</span><span class="sxs-lookup"><span data-stu-id="ffe00-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="ffe00-138">Další kroky</span><span class="sxs-lookup"><span data-stu-id="ffe00-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ffe00-139">Účastník</span><span class="sxs-lookup"><span data-stu-id="ffe00-139">Participant</span></span></td>
    <td><span data-ttu-id="ffe00-140">Uživatelé, kteří jsou přiřazeni k určité skupině nebo roli</span><span class="sxs-lookup"><span data-stu-id="ffe00-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffe00-141">Po výběru možnosti <strong>Účastník</strong> na kartě <strong>Založeno na roli</strong> v seznamu <strong>Typ účastníka</strong> vyberte typ skupiny nebo role, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="ffe00-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ffe00-142">V seznamu <strong>Účastník</strong> vyberte skupinu nebo roli, které chcete oznámení odeslat.</span><span class="sxs-lookup"><span data-stu-id="ffe00-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffe00-143">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="ffe00-143">Workflow user</span></span></td>
    <td><span data-ttu-id="ffe00-144">Uživatelé zúčastnění v aktuálním workflowu</span><span class="sxs-lookup"><span data-stu-id="ffe00-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ffe00-145">Po výběru možnosti <strong>Uživatel workflowu</strong> na kartě <strong>Uživatel workflowu</strong> v seznamu <strong>Uživatel workflowu</strong> vyberte uživatele, který se podílí na workflowu.</span><span class="sxs-lookup"><span data-stu-id="ffe00-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ffe00-146">Uživatel</span><span class="sxs-lookup"><span data-stu-id="ffe00-146">User</span></span></td>
    <td><span data-ttu-id="ffe00-147">Konkrétní uživatelé</span><span class="sxs-lookup"><span data-stu-id="ffe00-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ffe00-148">Po výběru možnosti <strong>Uživatel</strong> klepněte na kartu <strong>Uživatel</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffe00-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ffe00-149">Seznam <strong>Dostupní uživatelé</strong> obsahuje všechny uživatele.</span><span class="sxs-lookup"><span data-stu-id="ffe00-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="ffe00-150">Vyberte uživatele, kterým chcete odeslat oznámení, a pak přesuňte tyto uživatele do seznamu <strong>Vybraní uživatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="ffe00-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="ffe00-151">Zopakujte kroky 3 až 7 pro každou událost, kterou jste vybrali v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="ffe00-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>
