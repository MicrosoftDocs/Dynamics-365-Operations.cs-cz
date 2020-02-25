---
title: Konfigurace parametrů pracovního volna a absence
description: Definujte parametry lidských zdrojů pro pracovní volno a absenci v Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008337"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="bac24-103">Konfigurace parametrů pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="bac24-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="bac24-104">Před nastavením plánů pracovního volna a absencí v Dynamics 365 Human Resourcesje vhodné ověřit nastavení všech souvisejících parametrů lidských zdrojů, včetně následujících:</span><span class="sxs-lookup"><span data-stu-id="bac24-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="bac24-105">Číselná řada pro požadavky na pracovní volno</span><span class="sxs-lookup"><span data-stu-id="bac24-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="bac24-106">Nastavení zákona Opuštění z rodinných a lékařských důvodu (FMLA)</span><span class="sxs-lookup"><span data-stu-id="bac24-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="bac24-107">Nastavení samoobslužných služeb pro zaměstnance pro požadavky na pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="bac24-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="bac24-108">Parametry pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="bac24-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="bac24-109">Zobrazení a změna parametrů lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="bac24-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="bac24-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="bac24-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="bac24-111">V části **Nastavení** vyberte **parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="bac24-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="bac24-112">Na kartě **číselné řady** ověřte **kód číselné řady** pro **ID žádosti o pracovní volno** a podle potřeby jej změňte.</span><span class="sxs-lookup"><span data-stu-id="bac24-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="bac24-113">Toto nastavení určuje pořadí používané pro automatické přiřazování ID k žádostem o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="bac24-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="bac24-114">Na kartě **FMLA** ověřte nastavení FMLA a podle potřeby je změňte.</span><span class="sxs-lookup"><span data-stu-id="bac24-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="bac24-115">Na kartě **Samoobsluha zaměstnance** určete, zda manažeři mohou zadat žádosti o pracovní volno a absenci jménem svých zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="bac24-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="bac24-116">Na kartě **Pracovní volno a absence** ověřte nastavení FMLA a podle potřeby je změňte.</span><span class="sxs-lookup"><span data-stu-id="bac24-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="bac24-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bac24-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="bac24-118">Konfigurace parametrů kalendáře</span><span class="sxs-lookup"><span data-stu-id="bac24-118">Configure calendar parameters</span></span>

<span data-ttu-id="bac24-119">Pokud jste povolili funkci Náhled kalendáře pracovního volna a absencí, je nutné nakonfigurovat další parametry.</span><span class="sxs-lookup"><span data-stu-id="bac24-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="bac24-120">V případě verze Preview z 3. února 2020 jsou povoleny pouze **čekající žádosti o volno**.</span><span class="sxs-lookup"><span data-stu-id="bac24-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="bac24-121">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="bac24-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="bac24-122">V části **Nastavení** vyberte **parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="bac24-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="bac24-123">Na kartě **Kalendář** podle potřeby ověřte nastavení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="bac24-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="bac24-124">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="bac24-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="bac24-125">Viz také</span><span class="sxs-lookup"><span data-stu-id="bac24-125">See also</span></span>

- [<span data-ttu-id="bac24-126">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="bac24-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
