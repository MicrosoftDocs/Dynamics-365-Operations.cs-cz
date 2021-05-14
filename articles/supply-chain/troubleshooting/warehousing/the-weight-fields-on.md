---
title: Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu
description: Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924344"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="08bbb-103">Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu</span><span class="sxs-lookup"><span data-stu-id="08bbb-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="08bbb-104">Kódy chyb: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="08bbb-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="08bbb-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="08bbb-105">Symptoms</span></span>

<span data-ttu-id="08bbb-106">Systém zobrazuje následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="08bbb-106">The system shows the following error message:</span></span>

> <span data-ttu-id="08bbb-107">Pole hmotnosti na řádcích nákladu neodpovídají polím hmotnosti na nákladu %1.</span><span class="sxs-lookup"><span data-stu-id="08bbb-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="08bbb-108">Spusťte kontrolu konzistence hmotnosti nákladu skladu a přepočítejte pole hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="08bbb-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="08bbb-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="08bbb-109">Cause</span></span>

<span data-ttu-id="08bbb-110">Pole **Čistá hmotnost** a **Hmotnost obalu** jsou nastavena na řádku nákladu na hodnotu *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="08bbb-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="08bbb-111">Pole hmotnosti však nejsou nastavena na hodnotu *0* pro měření hmotnosti na produktu.</span><span class="sxs-lookup"><span data-stu-id="08bbb-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="08bbb-112">Pokud pole hmotnosti nejsou nastavena na řádku nákladu, jakékoli opravy množství na řádku nákladu mohou způsobit nesprávný výpočet hmotnosti na nákladu.</span><span class="sxs-lookup"><span data-stu-id="08bbb-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="08bbb-113">K tomuto problému může dojít, pokud se od vytvoření řádku nákladu změnily hmotnosti na produktu.</span><span class="sxs-lookup"><span data-stu-id="08bbb-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="08bbb-114">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="08bbb-114">Resolution</span></span>

<span data-ttu-id="08bbb-115">Ve výchozím nastavení se při vytváření řádku nákladu zadávají pole hmotnosti z produktu.</span><span class="sxs-lookup"><span data-stu-id="08bbb-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="08bbb-116">Pokud je hmotnost nulová, můžete ji přepočítat pomocí funkce *Kontrola konzistence hmotnosti nákladu skladu*.</span><span class="sxs-lookup"><span data-stu-id="08bbb-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="08bbb-117">Přejděte k nabídce **Správa systému \> Periodické úkoly \> Databáze \> Kontrola konzistence**.</span><span class="sxs-lookup"><span data-stu-id="08bbb-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="08bbb-118">V dialogovém okně **Kontrola konzistence** nastavte pole **Modul** na hodnotu *Řízení skladu*.</span><span class="sxs-lookup"><span data-stu-id="08bbb-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="08bbb-119">Nastavte pole **Kontrola / oprava** na hodnotu *Opravit chybu*.</span><span class="sxs-lookup"><span data-stu-id="08bbb-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="08bbb-120">V seznamu zaškrtávacích políček vyberte zaškrtávací políčko **Kontrola konzistence hmotnosti nákladu skladu** a ujistěte se, že je zvýrazněn pouze řádek pro toto zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="08bbb-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="08bbb-121">V horní části seznamu zaškrtávacích políček vyberte tlačítko se třemi tečkami (**...**) a poté v nabídce vyberte možnost **Dialogové okno**.</span><span class="sxs-lookup"><span data-stu-id="08bbb-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="08bbb-122">V dialogovém okně **Kontrola konzistence hmotnosti nákladu skladu** nastavte následující pole a určete kritéria, podle kterých by měla probíhat kontrola konzistence:</span><span class="sxs-lookup"><span data-stu-id="08bbb-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="08bbb-123">**ID nákladu:** Zadejte ID nákladu.</span><span class="sxs-lookup"><span data-stu-id="08bbb-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="08bbb-124">Chcete-li zkontrolovat všechna ID nákladu, ponechte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="08bbb-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="08bbb-125">**Číslo položky:** Zadejte číslo položky.</span><span class="sxs-lookup"><span data-stu-id="08bbb-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="08bbb-126">Chcete-li zkontrolovat všechny položky, ponechte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="08bbb-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="08bbb-127">**Vždy přepočítávat hmotnost nákladů:** Tuto možnost nastavte na hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="08bbb-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="08bbb-128">**Povolit přepsání hmotnosti na řádcích nákladu:** Tuto možnost nastavte na hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="08bbb-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="08bbb-129">Výběrem tlačítka **OK** zavřete dialogové okno **Kontrola konzistence hmotnosti nákladu skladu**.</span><span class="sxs-lookup"><span data-stu-id="08bbb-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="08bbb-130">Vyberte tlačítko se třemi tečkami a poté v nabídce vyberte možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="08bbb-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="08bbb-131">Hmotnost se přepočítá na základě zadaných kritérií.</span><span class="sxs-lookup"><span data-stu-id="08bbb-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="08bbb-132">Vyberte odkaz **Podrobnosti zprávy** k zobrazení výsledku kontroly konzistence.</span><span class="sxs-lookup"><span data-stu-id="08bbb-132">Select the **Message details** link to view the result of the consistency check.</span></span>
