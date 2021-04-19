---
title: Odstraňování problémů s prací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837434"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="47b7d-103">Odstraňování problémů s prací skladu</span><span class="sxs-lookup"><span data-stu-id="47b7d-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47b7d-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="47b7d-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="47b7d-105">Nemohu přesouvat registrační značky, které mají položky sériového čísla, když je ve skupině dimenze sledování povolen prázdný výdej a prázdná příjemka.</span><span class="sxs-lookup"><span data-stu-id="47b7d-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="47b7d-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="47b7d-106">Issue description</span></span>

<span data-ttu-id="47b7d-107">Registrační značku nelze přesunout pomocí položky nabídky **Přesun**, pokud má sériové číslo nastavení *Prázdný výdej povolen* a *Prázdná příjemka povolena* ve skupině dimenze sledování a pokud je na stejném místě více registračních značek, některé mají sériová čísla a některé je nemají.</span><span class="sxs-lookup"><span data-stu-id="47b7d-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="47b7d-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="47b7d-108">Issue resolution</span></span>

<span data-ttu-id="47b7d-109">Tento problém bude vyřešen změnami, které jsou nasazeny v [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="47b7d-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="47b7d-110">Tyto změny způsobí, že je pole **Sériové číslo** nepovinné, pokud jsou povoleny prázdné příjemky a prázdné výdeje.</span><span class="sxs-lookup"><span data-stu-id="47b7d-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="47b7d-111">Při zpracování pohybů se mi v mobilní aplikaci Řízení skladu zobrazí následující chybová zpráva: „Vlastník inventáře %1 v tomto procesu není povolen.“</span><span class="sxs-lookup"><span data-stu-id="47b7d-111">I receive the following error message in the Warehouse Management mobile app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="47b7d-112">Popis problému</span><span class="sxs-lookup"><span data-stu-id="47b7d-112">Issue description</span></span>

<span data-ttu-id="47b7d-113">Sledovací dimenze **Vlastník** chybí, když se mobilní aplikaci Řízení skladu používá k provádění přesunů.</span><span class="sxs-lookup"><span data-stu-id="47b7d-113">The **Owner** tracking dimension is missing when the Warehouse Management mobile app is used to make movements.</span></span> <span data-ttu-id="47b7d-114">Pravidelný deník přesunů zásob od klienta Supply Chain Management nejspíš funguje podle plánu a lze ho zaúčtovat, pouze pokud je vyplněna dimenze **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="47b7d-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="47b7d-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="47b7d-115">Issue resolution</span></span>

<span data-ttu-id="47b7d-116">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="47b7d-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="47b7d-117">V současné době procesy správy skladu podporují pouze zásoby, které jsou ve vlastnictví právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="47b7d-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]