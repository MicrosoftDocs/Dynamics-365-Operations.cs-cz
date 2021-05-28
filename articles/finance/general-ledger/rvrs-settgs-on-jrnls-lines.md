---
title: Nastavení storna deníků a řádků
description: Toto téma se zabývá důvodem, proč storno záznam, který byl zadán do hlavního deníku, nemusel být zahrnut do zaúčtované transakce.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028552"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="dc0c8-103">Nastavení storna deníků a řádků</span><span class="sxs-lookup"><span data-stu-id="dc0c8-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0c8-104">Toto téma se zabývá důvodem, proč storno záznam, který byl zadán do hlavního deníku, nemusel být zahrnut do zaúčtované transakce.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="dc0c8-105">Příznak</span><span class="sxs-lookup"><span data-stu-id="dc0c8-105">Symptom</span></span>

<span data-ttu-id="dc0c8-106">Hlavní deník zahrnuje storno záznam a datum stornování v deníku.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="dc0c8-107">Když deník zaúčtujete, nestornuje se žádný doklad.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="dc0c8-108">Proč tomu tak je?</span><span class="sxs-lookup"><span data-stu-id="dc0c8-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="dc0c8-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="dc0c8-109">Resolution</span></span>

<span data-ttu-id="dc0c8-110">Když se deník zaúčtovává, proces stornování se dívá pouze na nastavení **Storno záznamu** a **Datum stornování** v části **Řádky** dokladu.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="dc0c8-111">Tento přístup umožňuje deníku zahrnout některé doklady, které jsou označeny ke stornování, a jiné, které tak označeny nejsou.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="dc0c8-112">Hodnoty z deníku se při přidávání řádků jako *Nový* použijí pouze jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="dc0c8-113">Změna hodnot v deníku neovlivňuje existující řádky.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="dc0c8-114">V tomto příkladu byly nejprve zadány řádky dokladů.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="dc0c8-115">Když zadáte podrobnosti řádku před označením deníku jako stornování, označení jako storno záznamu a datum stornování se nepoužije na žádné existující řádky.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="dc0c8-116">Změna storno záznamu nebo data stornování na existujícím řádku šíří tuto změnu na další řádky ve stejném dokladu.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="dc0c8-117">K optimalizaci výkonu se mřížka po šíření změn na jiné řádky neaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="dc0c8-118">Aktualizované hodnoty můžete zobrazit aktualizováním mřížky.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-118">You can display the updated values by refreshing the grid.</span></span>


