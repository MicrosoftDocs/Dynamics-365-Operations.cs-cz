---
title: Vytvoření šeků se stavem bianko
description: Toto téma vysvětluje, jak vytvořit bianko šeky pro bankovní účet na stránce Šeky.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 47d54524f87cf718b9b41462b5133df267d5dd9e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570280"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="85896-103">Vytvoření šeků se stavem bianko</span><span class="sxs-lookup"><span data-stu-id="85896-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85896-104">Toto téma vysvětluje, jak vytvořit bianko šeky.</span><span class="sxs-lookup"><span data-stu-id="85896-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="85896-105">Můžete například vytvořit bianko šek pro zaznamenání šeku, který byl poškozen a nelze ho použít k platbě.</span><span class="sxs-lookup"><span data-stu-id="85896-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="85896-106">Na stránce **Šeky** můžete provádět úlohy údržby pro šeky.</span><span class="sxs-lookup"><span data-stu-id="85896-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="85896-107">Můžete například vytvářet nová čísla šeků a odstraňovat šeky.</span><span class="sxs-lookup"><span data-stu-id="85896-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="85896-108">Můžete též vytvářet šeky, které mají stav **Bianko**.</span><span class="sxs-lookup"><span data-stu-id="85896-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="85896-109">Po vytvoření bianko šeků nelze tyto šeky odstranit nebo je v systému použít znovu.</span><span class="sxs-lookup"><span data-stu-id="85896-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="85896-110">Tato funkce je k dispozici na stránce **Šeky** pouze tehdy, když zapnete funkci **Vytvoření šeků se stavem bianko na stránce Šeky** na stránce **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="85896-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="85896-111">Pokud není funkce zapnutá, lze šeky se stavem **Bianko** vytvořit pouze z dialogového okna **Platba šekem** během procesu generování platby v závazcích.</span><span class="sxs-lookup"><span data-stu-id="85896-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="85896-112">Chcete-li otevřít stránku **Šeky**, přejděte na **Pokladna a banka \> Bankovní účty \> Bankovní účty** a potom v podokně akcí na kartě **Řídit platby** ve skupině **Související informace** zvolte **Šeky**.</span><span class="sxs-lookup"><span data-stu-id="85896-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="85896-113">Nebo přejděte na **Pokladna a banka \> Dotazy a sestavy \> Šeky**.</span><span class="sxs-lookup"><span data-stu-id="85896-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="85896-114">Poté pro vytvoření šeků se stavem **Bianko** zvolte v podokně akcí možnost **Vytvořit bianko šeky**.</span><span class="sxs-lookup"><span data-stu-id="85896-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="85896-115">Když systém vytváří bianko šeky, je přidružený bankovní účet dočasně deaktivován.</span><span class="sxs-lookup"><span data-stu-id="85896-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="85896-116">Toto chování omezuje riziko vygenerování plateb ve stejné době, kdy se vytváří bianko šeky.</span><span class="sxs-lookup"><span data-stu-id="85896-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="85896-117">Po dokončení zpracování bude přidružený bankovní účet znovu aktivován.</span><span class="sxs-lookup"><span data-stu-id="85896-117">When the processing is completed, the associated bank account is reactivated.</span></span>
