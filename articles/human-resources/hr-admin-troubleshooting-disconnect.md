---
title: Odpojení klienta
description: Tento článek vysvětluje, jak postupovat při bezdůvodném odpojení odběratele od jeho prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2088706baf8735fa371960955a2ffc3240ccac76
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2020
ms.locfileid: "4417717"
---
# <a name="client-disconnects"></a><span data-ttu-id="c678c-103">Odpojení klienta</span><span class="sxs-lookup"><span data-stu-id="c678c-103">Client disconnects</span></span>

<span data-ttu-id="c678c-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="c678c-104">**Environment details**</span></span> 

<span data-ttu-id="c678c-105">Tento problém může nastat ve všech prostředích.</span><span class="sxs-lookup"><span data-stu-id="c678c-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="c678c-106">**Příznak**</span><span class="sxs-lookup"><span data-stu-id="c678c-106">**Symptom**</span></span> 

<span data-ttu-id="c678c-107">Odběratel je bezdůvodně odpojen od svého prostředí.</span><span class="sxs-lookup"><span data-stu-id="c678c-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="c678c-108">Odběratel obdrží jednu z následujících chybových zpráv:</span><span class="sxs-lookup"><span data-stu-id="c678c-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="c678c-109">Vaše připojení bylo ztraceno.</span><span class="sxs-lookup"><span data-stu-id="c678c-109">We've lost your connection.</span></span> <span data-ttu-id="c678c-110">Pokud chcete pokračovat v práci, klikněte na Zavřít.</span><span class="sxs-lookup"><span data-stu-id="c678c-110">Click Close to continue working.</span></span>
- <span data-ttu-id="c678c-111">Zdá se, že se přerušilo připojení k síti. Akci opakujte kliknutím na tlačítko Opakovat.</span><span class="sxs-lookup"><span data-stu-id="c678c-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="c678c-112">**Závažný problém**</span><span class="sxs-lookup"><span data-stu-id="c678c-112">**Red flag**</span></span>

<span data-ttu-id="c678c-113">K tomuto problému dochází často, když uživatelé jsou ve fázi implementace, porovnávají informace v produkčních a testovacích prostředích a zapomínají, že se pohybují mezi relacemi.</span><span class="sxs-lookup"><span data-stu-id="c678c-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="c678c-114">Pokud uživatelé jsou v této fázi, pravděpodobně se s tímto problémem setkají.</span><span class="sxs-lookup"><span data-stu-id="c678c-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="c678c-115">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="c678c-115">**Issue**</span></span> 

<span data-ttu-id="c678c-116">**Typy prohlížeče:** Google Chrome, Internet Explorer a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c678c-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="c678c-117">Microsoft Dynamics 365 Human Resources odpojuje uživatele, když jsou současně otevřeny dvě různé relace pro jednoho uživatele a stejný typ prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="c678c-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="c678c-118">(Například uživatel A zobrazuje prostředí 1 i 2 v prohlížeči Chrome.) Nezáleží na tom, zda uživatelé otevřenou jiná okna nebo jiné karty prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="c678c-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="c678c-119">Pokud se při přihlašování do prostředí 1 a prostředí 2 současně a ve stejném typu prohlížeče používají stejné přihlašovací údaje uživatele, aplikace Human Resources odpojí jednu z relací.</span><span class="sxs-lookup"><span data-stu-id="c678c-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="c678c-120">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="c678c-120">**Solution**</span></span>

<span data-ttu-id="c678c-121">Ujistěte se, že pro daný typ prohlížeče je současně otevřeno pouze jedno prostředí.</span><span class="sxs-lookup"><span data-stu-id="c678c-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="c678c-122">Uživatelé mohou otevřít více relací do stejného prostředí (více záložek ve stejném prohlížeči).</span><span class="sxs-lookup"><span data-stu-id="c678c-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="c678c-123">Uživatelé, kteří chtějí přeskakovat mezi dvěma prostředími současně, by měli otevřít každé prostředí v jiném typu prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="c678c-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="c678c-124">(Například uživatel A může zobrazit prostředí 1 v Chrome a prostředí 2 v Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="c678c-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
