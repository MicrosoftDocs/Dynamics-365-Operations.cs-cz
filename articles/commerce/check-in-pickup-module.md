---
title: Přihlášení k modulu vyzvednutí
description: Toto téma popisuje přihlášení pro modul vyzvednutí a popisuje, jak ho konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270576"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="147d3-103">Přihlášení k modulu vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="147d3-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="147d3-104">Toto téma popisuje přihlášení pro modul vyzvednutí a popisuje, jak ho konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="147d3-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="147d3-105">Modul přihlášení pro vyzvednutí poskytuje stránku s potvrzením pro zákazníky, kteří používají možnosti přihlášení zákazníka Dynamics 365 Commerce, aby obchod informoval o jejich příjezdu.</span><span class="sxs-lookup"><span data-stu-id="147d3-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="147d3-106">Modul přihlášení pro vyzvednutí také umožňuje nakonfigurovat formulář, který shromažďuje další informace od zákazníků, aby se usnadnilo doručení objednávky.</span><span class="sxs-lookup"><span data-stu-id="147d3-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="147d3-107">Tyto informace zahrnují číslo parkovacího místa zákazníka a značku a model jeho vozidla.</span><span class="sxs-lookup"><span data-stu-id="147d3-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="147d3-108">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="147d3-108">Module properties</span></span>

| <span data-ttu-id="147d3-109">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="147d3-109">Property name</span></span> | <span data-ttu-id="147d3-110">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="147d3-110">Values</span></span> | <span data-ttu-id="147d3-111">popis</span><span class="sxs-lookup"><span data-stu-id="147d3-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="147d3-112">Text potvrzení</span><span class="sxs-lookup"><span data-stu-id="147d3-112">Confirmation text</span></span> | <span data-ttu-id="147d3-113">Textový řetězec</span><span class="sxs-lookup"><span data-stu-id="147d3-113">Text string</span></span> | <span data-ttu-id="147d3-114">Obsah nadpisu, který se zobrazí na stránce s potvrzením ohlášení.</span><span class="sxs-lookup"><span data-stu-id="147d3-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="147d3-115">Zobrazit QR kód</span><span class="sxs-lookup"><span data-stu-id="147d3-115">Show QR code</span></span> | <span data-ttu-id="147d3-116">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="147d3-116">**True** or **False**</span></span> | <span data-ttu-id="147d3-117">Když je tato vlastnost nastavena na **True**, stránka pro potvrzení přihlášení zobrazuje QR kód, který představuje ID potvrzení objednávky.</span><span class="sxs-lookup"><span data-stu-id="147d3-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="147d3-118">Nadpis s dalšími informacemi</span><span class="sxs-lookup"><span data-stu-id="147d3-118">Additional information heading</span></span> | <span data-ttu-id="147d3-119">Textový řetězec</span><span class="sxs-lookup"><span data-stu-id="147d3-119">Text string</span></span> | <span data-ttu-id="147d3-120">Obsah nadpisu, který se zobrazí, když byla nakonfigurována další informační pole.</span><span class="sxs-lookup"><span data-stu-id="147d3-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="147d3-121">Další informační klíče</span><span class="sxs-lookup"><span data-stu-id="147d3-121">Additional information keys</span></span> | <span data-ttu-id="147d3-122">Dvojice ID zdroje / hodnota prostředku</span><span class="sxs-lookup"><span data-stu-id="147d3-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="147d3-123">Každý klíč vytváří pole formuláře a přidružený štítek, které se používají ke shromažďování dalších informací od zákazníků.</span><span class="sxs-lookup"><span data-stu-id="147d3-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="147d3-124">Další informační klíče \> ID zdroje</span><span class="sxs-lookup"><span data-stu-id="147d3-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="147d3-125">Textový řetězec</span><span class="sxs-lookup"><span data-stu-id="147d3-125">Text string</span></span> | <span data-ttu-id="147d3-126">Každý klíč informací vytváří pole formuláře a přidružený štítek, které se používají ke shromažďování dalších informací od zákazníků.</span><span class="sxs-lookup"><span data-stu-id="147d3-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="147d3-127">Tato vlastnost identifikuje klíč dalších informací.</span><span class="sxs-lookup"><span data-stu-id="147d3-127">This property identifies the additional information key.</span></span> <span data-ttu-id="147d3-128">V úloze, která je vytvořena v místě prodeje (POS), se hodnota této vlastnosti zobrazí jako popisek v poli s pokyny.</span><span class="sxs-lookup"><span data-stu-id="147d3-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="147d3-129">Další informační klíče \> Hodnota prostředku</span><span class="sxs-lookup"><span data-stu-id="147d3-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="147d3-130">Textový řetězec</span><span class="sxs-lookup"><span data-stu-id="147d3-130">Text string</span></span> | <span data-ttu-id="147d3-131">Popisek pro textové pole v úkolu v POS.</span><span class="sxs-lookup"><span data-stu-id="147d3-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="147d3-132">Další informační klíče \> Povinné</span><span class="sxs-lookup"><span data-stu-id="147d3-132">Additional information keys \> Required</span></span> | <span data-ttu-id="147d3-133">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="147d3-133">**True** or **False**</span></span> | <span data-ttu-id="147d3-134">Tato vlastnost určuje, zda musí zákazníci před pokračováním vyplnit pole formuláře.</span><span class="sxs-lookup"><span data-stu-id="147d3-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="147d3-135">Když je tato vlastnost nastavena na **True**, vedle popisku formuláře se vykreslí hvězdička a provede se nulová kontrola, aby se zabránilo pokračování zákazníků, pokud není zadána žádná hodnota.</span><span class="sxs-lookup"><span data-stu-id="147d3-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="147d3-136">Přidání modulu přihlášení pro vyzvednutí na stránku</span><span class="sxs-lookup"><span data-stu-id="147d3-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="147d3-137">Modul přihlášení pro vyzvednutí by měl být přidán na novou stránku, kterou vytvoříte pro potvrzení přihlášení.</span><span class="sxs-lookup"><span data-stu-id="147d3-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="147d3-138">Tato stránka bude sloužit jako prostředí s potvrzením přihlášení pro zákazníky, kteří vyberou odkaz **Jsem tady** nebo tlačítko v e-mailu.</span><span class="sxs-lookup"><span data-stu-id="147d3-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="147d3-139">Konfigurace formuláře s dalšími informacemi</span><span class="sxs-lookup"><span data-stu-id="147d3-139">Configure the additional information form</span></span>

<span data-ttu-id="147d3-140">Ve výchozím nastavení, pokud nejsou nakonfigurovány žádné další informační klíče, modul zobrazí zákazníkům stránku s potvrzením přihlášení.</span><span class="sxs-lookup"><span data-stu-id="147d3-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="147d3-141">Jakmile se zobrazí potvrzení o přihlášení, vytvoří se v POS úkol pro obchod, kde se vyzvedává objednávka.</span><span class="sxs-lookup"><span data-stu-id="147d3-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="147d3-142">Když je nakonfigurován jeden nebo více dalších informačních klíčů, zákazníci jsou nejprve vyzváni k zadání informací.</span><span class="sxs-lookup"><span data-stu-id="147d3-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="147d3-143">Když si vyberou **Odeslat**, zobrazí se jim potvrzení odbavení a v POS se vytvoří úkol.</span><span class="sxs-lookup"><span data-stu-id="147d3-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="147d3-144">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="147d3-144">Additional resources</span></span>

[<span data-ttu-id="147d3-145">Povolit oznámení o přihlášení zákazníka v místě prodeje (POS)</span><span class="sxs-lookup"><span data-stu-id="147d3-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
