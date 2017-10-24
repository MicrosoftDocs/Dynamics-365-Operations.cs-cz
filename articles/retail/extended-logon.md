---
title: "Nastavení funkce rozšířeného přihlášení pro Cloud POS a MPOS"
description: "Toto téma zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="2a659-103">Nastavení funkce rozšířeného přihlášení pro Cloud POS a MPOS</span><span class="sxs-lookup"><span data-stu-id="2a659-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2a659-104">Toto téma zahrnuje možnosti pro nastavení rozšířeného přihlášení pro systém Cloud POS a Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="2a659-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="2a659-105">Nastavení rozšířeného přihlášení</span><span class="sxs-lookup"><span data-stu-id="2a659-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="2a659-106">Nastavení masek čárových kódů najdete v části **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="2a659-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="2a659-107">Pevná záložka **Funkce** obsahuje následující volby, které se vztahují k rozšířenému přihlašování.</span><span class="sxs-lookup"><span data-stu-id="2a659-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="2a659-108">Přihlášení zaměstnance čárovým kódem</span><span class="sxs-lookup"><span data-stu-id="2a659-108">Staff bar code logon</span></span>

<span data-ttu-id="2a659-109">Pokud je aktivní možnost **Přihlášení zaměstnance čárovým kódem**, mohou se pracovníci s přiřazeným rozšířeným přihlášením přihlásit k jejich pokladnímu místu pomocí čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="2a659-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="2a659-110">Přihlášení zaměstnance pomocí čárového kódu vyžaduje heslo.</span><span class="sxs-lookup"><span data-stu-id="2a659-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="2a659-111">Pokud je povolena možnost **Přihlášení zaměstnance čárovým kódem vyžaduje heslo**, přihlášení zaměstnance čárovým kódem vybere pouze pracovníky, kterým je přiřazeno rozšířené přihlášení, která je uvedeno.</span><span class="sxs-lookup"><span data-stu-id="2a659-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="2a659-112">Když je toto políčko zaškrtnuto, zaměstnanci musí i nadále zadávat své heslo.</span><span class="sxs-lookup"><span data-stu-id="2a659-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="2a659-113">Přihlášení zaměstnance kartou</span><span class="sxs-lookup"><span data-stu-id="2a659-113">Staff card logon</span></span>

<span data-ttu-id="2a659-114">Pokud je aktivní možnost **Přihlášení zaměstnance kartou**, mohou se pracovníci s přiřazeným rozšířeným přihlášením přihlásit k jejich pokladnímu místu pomocí magnetického proužku.</span><span class="sxs-lookup"><span data-stu-id="2a659-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="2a659-115">Přihlášení zaměstnance pomocí karty vyžaduje heslo.</span><span class="sxs-lookup"><span data-stu-id="2a659-115">Staff card logon requires password</span></span>

<span data-ttu-id="2a659-116">Pokud je povolena možnost **Přihlášení zaměstnance pomocí karty vyžaduje heslo.**, přihlášení zaměstnance kartou vybere pouze pracovníky, kterým je přiřazeno rozšířené přihlášení, která je uvedeno.</span><span class="sxs-lookup"><span data-stu-id="2a659-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="2a659-117">Když je toto políčko zaškrtnuto, zaměstnanci musí i nadále zadávat své heslo.</span><span class="sxs-lookup"><span data-stu-id="2a659-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="2a659-118">Přiřazení rozšířeného přihlášení</span><span class="sxs-lookup"><span data-stu-id="2a659-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="2a659-119">Ve výchozím nastavení pouze manažeři mohou přiřadit rozšířené přihlášení zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="2a659-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="2a659-120">Chcete-li přiřadit rozšířené přihlášení, přejděte na **Rozšířené přihlášení** v POS.</span><span class="sxs-lookup"><span data-stu-id="2a659-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="2a659-121">Pak vyhledejte pracovníka zadáním jeho ID operátora do vyhledávacího pole.</span><span class="sxs-lookup"><span data-stu-id="2a659-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="2a659-122">Vyberte pracovníka a klikněte na možnost **Přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="2a659-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="2a659-123">Na další stránce protáhněte nebo naskenujte rozšířené přihlášení pro přiřazení pracovníka.</span><span class="sxs-lookup"><span data-stu-id="2a659-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="2a659-124">Pokud je protáhnutí nebo naskenování úspěšné, tlačítko **OK** bude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="2a659-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="2a659-125">Klepněte na tlačítko **OK** pro uložení rozšířeného přihlášení pro tohoto pracovníka.</span><span class="sxs-lookup"><span data-stu-id="2a659-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="2a659-126">Odstranění rozšířeného přihlášení</span><span class="sxs-lookup"><span data-stu-id="2a659-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="2a659-127">Pokud chcete odstranit rozšířené přihlášení přiřazené k pracovníkovi, vyhledejte pracovníka pomocí operace **Rozšířené přihlášení**.</span><span class="sxs-lookup"><span data-stu-id="2a659-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="2a659-128">Vyberte pracovníka a klikněte na možnost **Zrušit přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="2a659-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="2a659-129">Budou odebrány všechny rozšířené přihlašovací údaje, které jsou přidruženy k danému pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="2a659-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="2a659-130">Rozšíření rozšířeného přihlášení</span><span class="sxs-lookup"><span data-stu-id="2a659-130">Extending extended logon</span></span>
========================

<span data-ttu-id="2a659-131">Službu pro přihlášení lze rozšířit o podporu dalších zařízení pro rozšířené přihlášení, jako jsou čtečky dlaní.</span><span class="sxs-lookup"><span data-stu-id="2a659-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="2a659-132">Další informace naleznete v dokumentaci k rozšíření služby POS.</span><span class="sxs-lookup"><span data-stu-id="2a659-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="2a659-133">Používání rozšířeného přihlášení</span><span class="sxs-lookup"><span data-stu-id="2a659-133">Using extended logon</span></span>
====================

<span data-ttu-id="2a659-134">Jakmile je rozšířené přihlášení nakonfigurováno a pracovník má přiřazen čárový kód nebo magnetický proužek, pracovníkovi stačí pouze protáhnout nebo naskenovat svoji kartu po zobrazení přihlašovací stránky POS.</span><span class="sxs-lookup"><span data-stu-id="2a659-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="2a659-135">Je-li ke zpracování přihlášení nutné také heslo, pracovník je vyzván k zadání svého hesla.</span><span class="sxs-lookup"><span data-stu-id="2a659-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




