---
title: Přiřadit role uživatele leasingu
description: Toto téma popisuje role zabezpečení, které se používají pro leasing majetku. Vysvětluje také, jak těmto rolím přiřadit uživatele.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 09d80e9629b60144665441989d9d63d7f6be3c60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207272"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="662ee-104">Přiřadit role uživatele leasingu</span><span class="sxs-lookup"><span data-stu-id="662ee-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="662ee-105">Toto téma popisuje role zabezpečení, které se používají pro leasing majetku.</span><span class="sxs-lookup"><span data-stu-id="662ee-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="662ee-106">Vysvětluje také, jak těmto rolím přiřadit uživatele.</span><span class="sxs-lookup"><span data-stu-id="662ee-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="662ee-107">Při leasingu majetku rozlišují přístup tři uživatelské role.</span><span class="sxs-lookup"><span data-stu-id="662ee-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="662ee-108">Jedna role je vhodná pro udržování leasingu, druhá je vhodná pro prohlížení leasingu a druhá je vhodná pro plnění povinností referenta leasingu.</span><span class="sxs-lookup"><span data-stu-id="662ee-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="662ee-109">Každá role má specifická oprávnění pro všechny stránky leasingu a každá umožňuje uživatelům prohlížet, vytvářet, upravovat nebo mazat leasingy podle svých pracovních povinností.</span><span class="sxs-lookup"><span data-stu-id="662ee-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="662ee-110">Role</span><span class="sxs-lookup"><span data-stu-id="662ee-110">Role</span></span>           | <span data-ttu-id="662ee-111">popis</span><span class="sxs-lookup"><span data-stu-id="662ee-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="662ee-112">Údržba leasingu</span><span class="sxs-lookup"><span data-stu-id="662ee-112">Maintain Lease</span></span> | <span data-ttu-id="662ee-113">Uživatelé v této roli mohou přidávat, upravovat, mazat a zobrazovat leasingy.</span><span class="sxs-lookup"><span data-stu-id="662ee-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="662ee-114">Tato role je určena pro každodenní uživatele, jejichž úkoly zahrnují vytváření a zveřejňování měsíčních záznamů deníku a přidávání nových leasingů.</span><span class="sxs-lookup"><span data-stu-id="662ee-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="662ee-115">Tato role umožňuje přístup ke všem funkcím leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="662ee-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="662ee-116">Zobrazit leasing</span><span class="sxs-lookup"><span data-stu-id="662ee-116">View Lease</span></span>     | <span data-ttu-id="662ee-117">Uživatelé v této roli mohou prohlížet pouze záznamy leasingu, plány a spouštět sestavy.</span><span class="sxs-lookup"><span data-stu-id="662ee-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="662ee-118">Nemohou vytvářet nové leasingy, upravovat stávající leasingy ani vytvářet záznamy deníku proti leasingům.</span><span class="sxs-lookup"><span data-stu-id="662ee-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="662ee-119">Role je navržena pro uživatele, kteří musí pouze zobrazit leasingy, plány leasingu a transakce, které se proti těmto leasingům vyskytnou.</span><span class="sxs-lookup"><span data-stu-id="662ee-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="662ee-120">Referent leasingu</span><span class="sxs-lookup"><span data-stu-id="662ee-120">Lease Clerk</span></span>    | <span data-ttu-id="662ee-121">Uživatelé v této roli mohou pouze vytvářet nové leasingy.</span><span class="sxs-lookup"><span data-stu-id="662ee-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="662ee-122">Nemohou upravovat ani mazat existující leasingy, prohlížet plány leasingů ani zveřejňovat položky deníku leasingu.</span><span class="sxs-lookup"><span data-stu-id="662ee-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="662ee-123">Tato role je určena pro uživatele, kteří pracují v kapacitě pro zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="662ee-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="662ee-124">Podle těchto pokynů můžete uživatelům přiřadit role, které se používají při leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="662ee-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="662ee-125">Přejděte na **Správa systému \> Zabezpečení \> Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="662ee-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="662ee-126">Vyberte role **Údržba leasingu**, **Referent leasingu** nebo **Zobrazit leasing** a poté vyberte **Ručně přiřadit / vyloučit uživatele**.</span><span class="sxs-lookup"><span data-stu-id="662ee-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="662ee-127">Vyberte uživatele, kterému chcete roli přiřadit, a poté vyberte **Přiřait k roli**.</span><span class="sxs-lookup"><span data-stu-id="662ee-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]