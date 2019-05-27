---
title: Pozastavení a obnovení transakce v POS
description: Toto téma vysvětluje, jak mohou uživatelé pozastavit probíhající transakce a obnovit je později nebo v jiné registrační pokladně pomocí aplikace Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569537"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="9b0f6-103">Pozastavení a obnovení transakcí v pokladním místě (POS)</span><span class="sxs-lookup"><span data-stu-id="9b0f6-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="9b0f6-104">Uživatelé pokladního místa mohou pozastavit probíhající transakce a následně je obnovit v jiné pokladně.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="9b0f6-105">Transakce jsou často pozastaveny, aby mohly rychle uvolnit registr pro jinou úlohu bez ztráty pokroku u aktuální transakce.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="9b0f6-106">Zaměstnanec prodejny například začne zpracovávat transakci zákazníka na mobilním zařízení, ale musí ji dokončit na pokladně, která má zásuvku s hotovostí.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="9b0f6-107">V takovém případě zaměstnanec obchodu může pozastavit transakci v mobilním zařízení a pak ji vyvolat a obnovit v registrační pokladně.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="9b0f6-108">Konfigurovat funkci pozastavení a obnovení</span><span class="sxs-lookup"><span data-stu-id="9b0f6-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="9b0f6-109">Operace POS</span><span class="sxs-lookup"><span data-stu-id="9b0f6-109">POS operations</span></span>

<span data-ttu-id="9b0f6-110">Dvě [operace POS](pos-operations.md) umožňují POS podporu scénářů pozastavení a pokračování.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="9b0f6-111">Tyto operace můžete přiřadit k [tlačítkům mřížky](pos-screen-layouts.md) na stránce transakce nebo na úvodní stránce.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="9b0f6-112">503: Pozastavit transakci</span><span class="sxs-lookup"><span data-stu-id="9b0f6-112">503: Suspend transaction</span></span>
- <span data-ttu-id="9b0f6-113">504: Odvolat transakci</span><span class="sxs-lookup"><span data-stu-id="9b0f6-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="9b0f6-114">Šablona příjmu</span><span class="sxs-lookup"><span data-stu-id="9b0f6-114">Receipt template</span></span>

<span data-ttu-id="9b0f6-115">POS lze konfigurovat tak, aby se po pozastavení transakce generoval vytištěný doklad.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="9b0f6-116">Tento doklad pak slouží k rychlé identifikaci a pozdějšímu odvolání transakce.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="9b0f6-117">Pokud chcete POS povolit tisk dokladu, musíte přidat formát potvrzení **pozastavení transakce** do profilu potvrzení v prodejně.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="9b0f6-118">Formát dokladu můžete navrhnout tak, aby obsahoval nebo vylučoval konkrétní detaily transakce.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="9b0f6-119">Formát může například obsahovat čárový kód podporující skenování.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="9b0f6-120">Číslování účtenek</span><span class="sxs-lookup"><span data-stu-id="9b0f6-120">Receipt numbering</span></span>

<span data-ttu-id="9b0f6-121">Stejně jako u ostatních typů transakcí POS, které generují tištěný doklad, můžete definovat číselnou sekvenci pozastavených transakcí v oddílu **Číslování dokladů** profilu funkce prodejny.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="9b0f6-122">Anulovat při uzávěrce směny</span><span class="sxs-lookup"><span data-stu-id="9b0f6-122">Void when closing shift</span></span>

<span data-ttu-id="9b0f6-123">Pomocí možnosti **Anulovat při zavření směny** můžete požadovat, aby uživatelé dokončili nebo anulovali jakékoli pozastavené transakce před uzavřením směny.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="9b0f6-124">Během operace **Zavřít směnu** POS vyzve uživatele k zobrazení nebo zrušení všech zbývajících pozastavených transakcí.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="9b0f6-125">Pozastavení a obnovení transakce</span><span class="sxs-lookup"><span data-stu-id="9b0f6-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="9b0f6-126">Pozastavení transakce</span><span class="sxs-lookup"><span data-stu-id="9b0f6-126">Suspend a transaction</span></span>

<span data-ttu-id="9b0f6-127">Uživatelé, kteří mají dostatečná oprávnění a rozložení obrazovky zahrnující operaci **Pozastavit transakci**, mohou pozastavit transakci a později ji vyvolat v jiném registru.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="9b0f6-128">Transakce lze pozastavit, pouze pokud **neobsahují** následující typy řádků:</span><span class="sxs-lookup"><span data-stu-id="9b0f6-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="9b0f6-129">Aktivní řádky platby</span><span class="sxs-lookup"><span data-stu-id="9b0f6-129">Active payment lines</span></span>
- <span data-ttu-id="9b0f6-130">Řádky dárkového poukazu (buď pro vydání dárkového poukazu nebo přidání k zůstatku dárkového poukazu)</span><span class="sxs-lookup"><span data-stu-id="9b0f6-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="9b0f6-131">Pozastavená transakce nemá vliv na informace o prodeji nebo informace o dostupnosti zásob pro obchod.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="9b0f6-132">Obnovení pozastavené transakce</span><span class="sxs-lookup"><span data-stu-id="9b0f6-132">Resume a suspended transaction</span></span>

<span data-ttu-id="9b0f6-133">Pozastavené transakce může odvolat a obnovit každý uživatel, který má dostatečná oprávnění, a který má také rozvržení, které obsahuje operaci **odvolat transakci**.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="9b0f6-134">Pokud chcete rychle a snadno vyvolat pozastavenou transakci, naskenujte čárový kód na vytištěném dokladu při zobrazení seznamu transakcí z operace **Odvolat transakci**.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="9b0f6-135">Co je třeba zvážit pro režim offline</span><span class="sxs-lookup"><span data-stu-id="9b0f6-135">Considerations for offline mode</span></span>

- <span data-ttu-id="9b0f6-136">Jakákoli transakce, která je pozastavena při POS v online režimu, nemůže být obnovena v režimu offline, protože data nejsou synchronizovaná s offline databází.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="9b0f6-137">Pokud pozastavíte transakci, když je POS v režimu offline, můžete ji odvolat v režimu offline za předpokladu, že POS nebyla převedena zpět režimu online od okamžiku pozastavení transakce.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="9b0f6-138">Po přepnutí POS zpět do režimu online se údaje o pozastavených transakcích přesunou do online databáze a jsou odebrány z offline databáze.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="9b0f6-139">Transakce lze tedy obnovit pouze v režimu online.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="9b0f6-140">Pokud přesunete POS zpět do režimu online, nebude možné pokračovat v této pozastavené transakci vzhledem k tomu, že již byly odebrány z offline databáze.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="9b0f6-141">Anulování pozastavené transakce</span><span class="sxs-lookup"><span data-stu-id="9b0f6-141">Void a suspended transaction</span></span>

<span data-ttu-id="9b0f6-142">Anulované transakce můžete zrušit tak, že transakci odvoláte a pak provedete operaci **Anulování transakce** nebo vyberete transakci v seznamu **Odvolat transakci** a na panelu aplikace vyberete **Anulovat**.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="9b0f6-143">Případně lze nakonfigurovat obchod tak, aby vyzval uživatele k anulování pozastavené transakce při uzavření směny.</span><span class="sxs-lookup"><span data-stu-id="9b0f6-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
