---
title: Kódy kroku vlny
description: V tomto tématu je uveden přehled kódů kroků vlny a jejich použití.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992350"
---
# <a name="wave-step-codes"></a><span data-ttu-id="d1a59-103">Kódy kroku vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="d1a59-104">Informace o kódech kroků vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-104">About wave step codes</span></span>

<span data-ttu-id="d1a59-105">Kódy kroků vlny jsou kódy, které mohou uživatelé nastavit a použít k propojení určitých instancí metod vlny s odpovídající šablonou.</span><span class="sxs-lookup"><span data-stu-id="d1a59-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="d1a59-106">Tyto šablony zahrnují šablony pro doplnění, vytváření kontejnerů, tisk štítků, sestavení a třídění.</span><span class="sxs-lookup"><span data-stu-id="d1a59-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="d1a59-107">Nejsou-li kódy kroků vlny použity, uživatelé musí zadat volný text, který bude odkazovat na určitou šablonu z instance metody vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="d1a59-108">Volný text je náchylný k chybám, protože uživatelé se musí ujistit, že text kroku vlny, který přidávají pro specifickou metodu vlny v šabloně vlny, přesně odpovídá textu kroku vlny v cílové šabloně.</span><span class="sxs-lookup"><span data-stu-id="d1a59-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="d1a59-109">Kódy kroků vlny pro určitý typ kroku vlny jsou nastaveny na samostatné stránce.</span><span class="sxs-lookup"><span data-stu-id="d1a59-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="d1a59-110">Pro každou instanci metody kroku vlny v šabloně vlny, která vyžaduje kód kroku vlny, musí být v rozevíracím seznamu vybrán kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="d1a59-111">Výběr v rozevíracím seznamu nahrazuje zadávání volného textu a pomáhá snižovat riziko a dopad lidských chyb.</span><span class="sxs-lookup"><span data-stu-id="d1a59-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="d1a59-112">Kódy nastavení se používají k propojení metody kroku vlny v šabloně vlny s cílovou šablonou pro metodu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="d1a59-113">Použití funkce kódů kroků vlny je volitelné a přijetí je pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="d1a59-114">Pokud tedy určitá právnická osoba používá funkci, budou všechny stávající kódy kroků vlny v dané právnické osobě upgradovány na novou strukturu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="d1a59-115">Nastavení ukázky</span><span class="sxs-lookup"><span data-stu-id="d1a59-115">Setup demo</span></span> 

<span data-ttu-id="d1a59-116">Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="d1a59-117">Povolit kódy kroku vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-117">Enable wave step codes</span></span>

<span data-ttu-id="d1a59-118">Pomocí následujících kroků zapněte funkci kódů kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="d1a59-119">Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="d1a59-120">Na kartě **Obecné** na pevné záložce **Zpracování vlny** nastavte možnost **Povolit kódy vlny** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="d1a59-121">Všechny existující volné texty kódu vlny jsou upgradovány na novou strukturu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="d1a59-122">Po dokončení tohoto upgradu pro právnickou osobu již není na možnost **Povolit kódy kroku vlny** na stránce **Parametry řízení skladu** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d1a59-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="d1a59-123">Ověření jsou prováděna během upgradu a pokud se upgrade nezdaří, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="d1a59-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="d1a59-124">Upgrade se nemusí zdařit kvůli následujícím konfliktům:</span><span class="sxs-lookup"><span data-stu-id="d1a59-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="d1a59-125">Existují duplicitní texty volného kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="d1a59-126">Existují přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="d1a59-126">Customizations exist.</span></span>
- <span data-ttu-id="d1a59-127">Volný text v kroku vlny, který je přidružen k instanci metody kroku vlny, neodpovídá očekávanému typu šablony.</span><span class="sxs-lookup"><span data-stu-id="d1a59-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="d1a59-128">Po vyřešení konfliktů, které byly zjištěny během ověření, můžete znovu spustit proces upgradu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="d1a59-129">Po úspěšném dokončení upgradu bude k dispozici stránka **kódy kroků vlny** (**Řízení skladu \> Nastavení \> Vlny \> Kódy nastavení vlny**).</span><span class="sxs-lookup"><span data-stu-id="d1a59-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="d1a59-130">Na této stránce jsou uvedeny kódy kroků vlny, které byly upgradovány při zapnutí funkce kódy kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="d1a59-131">Vytvořit nové kódy kroků vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-131">Create new wave step codes</span></span>

<span data-ttu-id="d1a59-132">Stránku **kódy kroků vlny** můžete použít k vytváření a odstraňování kódů kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="d1a59-133">Každý nový kód kroku vlny a jeho přidružené ID musí být jedinečné napříč všemi typy kroků vlny a musí být definovány pro určitý typ kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="d1a59-134">Použití kódů kroků vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-134">Apply wave step codes</span></span>

<span data-ttu-id="d1a59-135">Po definování příslušných kódů kroků vlny je lze použít na metody procesu vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="d1a59-136">Chcete-li použít kódy kroků vlny, přejděte na příslušnou cílovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="d1a59-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="d1a59-137">Zde jsou cílové šablony, pro které jsou označeny kódy kroků vlny na:</span><span class="sxs-lookup"><span data-stu-id="d1a59-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="d1a59-138">**Šablony doplnění:** Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění</span><span class="sxs-lookup"><span data-stu-id="d1a59-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="d1a59-139">**Načíst šablony sestavení:** Řízení skladu \> Nastavení \> Načíst \> Načíst šablony sestavení</span><span class="sxs-lookup"><span data-stu-id="d1a59-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="d1a59-140">**Seřadit šablony:** Řízení skladu \> Nastavení \> Balení \> Odchozí šablony řazení</span><span class="sxs-lookup"><span data-stu-id="d1a59-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="d1a59-141">**Šablony vytváření kontejnerů:** Řízení skladu \> Nastavení \> Kontejnery \> Šablony sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="d1a59-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="d1a59-142">**Štítky pro tisk štítků**: Řízení skladu \> Nastavení \> Směrování dokumentu \> Šablony štítku vlny</span><span class="sxs-lookup"><span data-stu-id="d1a59-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="d1a59-143">Šablony v tomto seznamu jsou použity, pokud jsou odkazovány z metody procesu vlny vybrané v šabloně vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="d1a59-144">Když kód kroku vlny u metody procesu vlny v šabloně vlny odpovídá kódu kroku vlny v jednom z typů šablon, použije se šablona.</span><span class="sxs-lookup"><span data-stu-id="d1a59-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="d1a59-145">Ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="d1a59-145">Sample scenario</span></span>

<span data-ttu-id="d1a59-146">Následující postup vám pomůže zaručit, že vytvořená šablona doplnění bude použita pro šablonu vlny.</span><span class="sxs-lookup"><span data-stu-id="d1a59-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="d1a59-147">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny** a vytvořte kód kroku vlny pro typ **doplnění**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="d1a59-148">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění** a vytvořte šablonu doplnění.</span><span class="sxs-lookup"><span data-stu-id="d1a59-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="d1a59-149">V šabloně doplnění vyberte kód kroku vlny, který jste vytvořili pro typ **doplnění**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="d1a59-150">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny** a vyberte šablonu vlny, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="d1a59-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="d1a59-151">V šabloně na pevné záložce **Metody** vyberte metodu **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="d1a59-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="d1a59-152">V poli **Kód kroku vlny** vyberte kód kroku vlny, který jste vybrali v šabloně doplnění.</span><span class="sxs-lookup"><span data-stu-id="d1a59-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
