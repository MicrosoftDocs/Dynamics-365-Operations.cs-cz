---
title: Odstraňování problémů s prací skladu
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970224"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="34228-103">Odstraňování problémů s prací skladu</span><span class="sxs-lookup"><span data-stu-id="34228-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34228-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s prací skladu v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34228-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="34228-105">Nemohu přesouvat registrační značky, které mají položky sériového čísla, když je ve skupině dimenze sledování povolen prázdný výdej a prázdná příjemka.</span><span class="sxs-lookup"><span data-stu-id="34228-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="34228-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="34228-106">Issue description</span></span>

<span data-ttu-id="34228-107">Registrační značku nelze přesunout pomocí položky nabídky **Přesun**, pokud má sériové číslo nastavení *Prázdný výdej povolen* a *Prázdná příjemka povolena* ve skupině dimenze sledování a pokud je na stejném místě více registračních značek, některé mají sériová čísla a některé je nemají.</span><span class="sxs-lookup"><span data-stu-id="34228-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="34228-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="34228-108">Issue resolution</span></span>

<span data-ttu-id="34228-109">Tento problém bude vyřešen změnami, které jsou nasazeny v [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="34228-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="34228-110">Tyto změny způsobí, že je pole **Sériové číslo** nepovinné, pokud jsou povoleny prázdné příjemky a prázdné výdeje.</span><span class="sxs-lookup"><span data-stu-id="34228-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="34228-111">Při zpracování pohybů se mi v aplikaci skladu zobrazí následující chybová zpráva: „Vlastník inventáře %1 v tomto procesu není povolen.“</span><span class="sxs-lookup"><span data-stu-id="34228-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="34228-112">Popis problému</span><span class="sxs-lookup"><span data-stu-id="34228-112">Issue description</span></span>

<span data-ttu-id="34228-113">Sledovací dimenze **Vlastník** chybí, když se aplikace skladu používá k provádění přesunů.</span><span class="sxs-lookup"><span data-stu-id="34228-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="34228-114">Pravidelný deník přesunů zásob od klienta Supply Chain Management nejspíš funguje podle plánu a lze ho zaúčtovat, pouze pokud je vyplněna dimenze **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="34228-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="34228-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="34228-115">Issue resolution</span></span>

<span data-ttu-id="34228-116">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="34228-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="34228-117">V současné době procesy správy skladu podporují pouze zásoby, které jsou ve vlastnictví právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="34228-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
