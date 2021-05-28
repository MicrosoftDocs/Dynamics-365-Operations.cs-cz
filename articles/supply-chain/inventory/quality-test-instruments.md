---
title: Testovací přístroje pro řízení kvality
description: Toto téma popisuje, jak vytvořit testovací přístroje, které bude možné použít pro testy na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021725"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="3b84f-103">Testovací přístroje pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="3b84f-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b84f-104">Toto téma popisuje, jak vytvořit testovací přístroje, které bude možné použít pro testy na objednávkách kvality v softwaru Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3b84f-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="3b84f-105">Použijte stránku **Testovací přístroje** pro definování a zobrazení podrobností o zařízeních, která se používají k provádění testů na objednávkách kvality.</span><span class="sxs-lookup"><span data-stu-id="3b84f-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="3b84f-106">Testovací přístroje jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="3b84f-106">Test instruments are optional.</span></span> <span data-ttu-id="3b84f-107">Mohou však pomoci dát pracovníkům kvality vědět, které zařízení nebo nástroj by měli použít k provedení konkrétního testu.</span><span class="sxs-lookup"><span data-stu-id="3b84f-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="3b84f-108">Příklad testovacího přístroje</span><span class="sxs-lookup"><span data-stu-id="3b84f-108">Test instrument example</span></span>

<span data-ttu-id="3b84f-109">Provádíte různé testy elektrických komponent.</span><span class="sxs-lookup"><span data-stu-id="3b84f-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="3b84f-110">Některé testy se týkají napěťového výstupu komponent, jeden test jejich teploty a jeden test jejich hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="3b84f-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="3b84f-111">K provedení jednotlivých testů se používají různé nástroje, zařízení nebo vybavení.</span><span class="sxs-lookup"><span data-stu-id="3b84f-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="3b84f-112">Například pro měření napětí se používá voltmetr, pro měření teploty teploměr a pro měření hmotnosti se používá váha.</span><span class="sxs-lookup"><span data-stu-id="3b84f-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="3b84f-113">Každé z těchto zařízení můžete nakonfigurovat jako testovací přístroj a označit měrnou jednotku, ve které by měly být zaznamenány výsledky testu.</span><span class="sxs-lookup"><span data-stu-id="3b84f-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="3b84f-114">Například výsledky z voltmetru se zaznamenávají ve voltech, výsledky z teploměru se zaznamenávají ve stupních Fahrenheita nebo stupňů Celsia a výsledky z váhy se zaznamenávají v librách nebo kilogramech.</span><span class="sxs-lookup"><span data-stu-id="3b84f-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="3b84f-115">Vytvoření testovacího přístroje</span><span class="sxs-lookup"><span data-stu-id="3b84f-115">Create a test instrument</span></span>

1. <span data-ttu-id="3b84f-116">Přejděte k nabídce **Řízení zásob \> Nastavení \> Řízení kvality \> Testovací přístroje**.</span><span class="sxs-lookup"><span data-stu-id="3b84f-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="3b84f-117">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="3b84f-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="3b84f-118">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="3b84f-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="3b84f-119">**Testovací přístroj** – zadejte jedinečné ID nebo název testovacího přístroje.</span><span class="sxs-lookup"><span data-stu-id="3b84f-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="3b84f-120">**Popis** – zadejte podrobný popis testovacího přístroje.</span><span class="sxs-lookup"><span data-stu-id="3b84f-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="3b84f-121">**Jednotka** – vyberte jednotku, ve které přístroj měří výsledky.</span><span class="sxs-lookup"><span data-stu-id="3b84f-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="3b84f-122">Pole **Přesnost** se nastaví automaticky na základě jednotky, kterou vyberete.</span><span class="sxs-lookup"><span data-stu-id="3b84f-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="3b84f-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3b84f-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b84f-124">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3b84f-124">Additional resources</span></span>

- [<span data-ttu-id="3b84f-125">Test správy kvality</span><span class="sxs-lookup"><span data-stu-id="3b84f-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="3b84f-126">Testovací skupiny pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="3b84f-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
