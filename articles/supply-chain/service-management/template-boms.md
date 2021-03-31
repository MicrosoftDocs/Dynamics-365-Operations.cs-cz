---
title: Kusovníky šablony
description: Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 574a9e38b7b820e8a0e7d188396d095570c21e94
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214243"
---
# <a name="template-boms"></a><span data-ttu-id="3e3d8-103">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="3e3d8-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3e3d8-104">Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="3e3d8-105">Součásti uvedené v kusovníku šablony představují jednotlivé dílčí součásti předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="3e3d8-106">Když na předmět servisu použijete kusovník šablony, můžete uchovávat záznam dílčích součástí, které byly v předmětu servisu vyměněny.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="3e3d8-107">Použití kusovníku šablony na servisní smlouvu nebo zakázku vyžaduje jeho připojení ke vztahu předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3e3d8-108">Na předmět servisu lze použít pouze jeden kusovník šablony.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="3e3d8-109">Vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-109">Create a template BOM</span></span>

<span data-ttu-id="3e3d8-110">Následující tabulka obsahuje informace o různých metodách používaných k vytvoření šablony Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e3d8-111">Metoda</span><span class="sxs-lookup"><span data-stu-id="3e3d8-111">Method</span></span></p></th>
<th><p><span data-ttu-id="3e3d8-112">popis</span><span class="sxs-lookup"><span data-stu-id="3e3d8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e3d8-113">Výrobní</span><span class="sxs-lookup"><span data-stu-id="3e3d8-113">Production</span></span></p></td>
<td><p><span data-ttu-id="3e3d8-114">Šablona kusovníku je založena na výrobní zakázce.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="3e3d8-115">Tato možnost je k dispozici pouze v případě, že pracujete v produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="3e3d8-116">Výhodou je, že máte aktuální, podrobný seznam součástí, které tvoří položku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3d8-117">Položka BOM</span><span class="sxs-lookup"><span data-stu-id="3e3d8-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="3e3d8-118">Šablona kusovníku je vytvořena na základě kusovníku položky.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="3e3d8-119">Kusovník položky, na rozdíl od výrobního Kusovníku, je statický seznam součástí, ze kterých je položka sestavena.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e3d8-120">Stávající šablona</span><span class="sxs-lookup"><span data-stu-id="3e3d8-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="3e3d8-121">Tato šablona je vytvořena na základě existujícího kusovníku položky.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e3d8-122">Ruční</span><span class="sxs-lookup"><span data-stu-id="3e3d8-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="3e3d8-123">Pokud víte, které náhradní díly obvykle měníte v předmětu servisu, můžete ručně vytvořit šablonu kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="3e3d8-124">Tato metoda napomáhá k zajištění, že součásti, které jsou zahrnuty do šablony, odpovídají skutečným požadavkům vašeho pracoviště.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="3e3d8-125">Použití kusovníku šablony na servisní smlouvu nebo zakázku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="3e3d8-126">Kusovník šablony můžete použít na servisní smlouvu nebo servisní zakázku nebo na obojí.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="3e3d8-127">Servisní smlouva obvykle pokrývá dlouhodobou spolupráci s odběratelem.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="3e3d8-128">Užitečnými informacemi, které je třeba zaznamenat v servisní smlouvě, je historie výměn, která jsou sledovány v servisním kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="3e3d8-129">Šablonu Kusovníku lze také použít na servisní zakázku a zaznamenávat historii služby, která byla provedena v předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="3e3d8-130">Zkopírování historie servisního kusovníku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="3e3d8-131">Historii řádků servisního kusovníku lze zkopírovat z jedné servisní smlouvy do jiné smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="3e3d8-132">Zkopírováním historie servisu mezi smlouvami můžete zachovat záznam o výměnách položky.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="3e3d8-133">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="3e3d8-133">**Example**</span></span>

<span data-ttu-id="3e3d8-134">Uzavřeli jste tříletou servisní smlouvu na auto odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="3e3d8-135">Během tohoto období si odběratel zvykne na vysokou úroveň služeb, kterou společnost poskytuje.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="3e3d8-136">Proto po vypršení smlouvy chce tento zákazník zadat novou.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="3e3d8-137">Máte nyní možnost dohodnout výhodnější smluvní podmínky pro společnost.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="3e3d8-138">Vzhledem k tomu, že záznamy o vyměněných součástech mohou být v budoucnosti užitečné, zkopírujete historii servisního kusovníku do nové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="3e3d8-139">Úprava kusovníku šablony</span><span class="sxs-lookup"><span data-stu-id="3e3d8-139">Modify the template BOM</span></span>

<span data-ttu-id="3e3d8-140">Pokud šablona Kusovníku nebyla připojena k předmětu servisu, můžete z ní upravit nebo odstranit řádky.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="3e3d8-141">Po připojení šablony Kusovníku k určitému předmětu servisu můžete upravit místní verzi Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="3e3d8-142">Pokud chcete duplikovat nastavení místní verze Kusovníku šablony, můžete vytvořit novou šablonu Kusovníku na základě místní verze.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="3e3d8-143">Další informace získáte v tématu [Změna kusovníku služby](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="3e3d8-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="3e3d8-144">Pokud nahradíte položku v kusovníku, můžete výměnu zaznamenat v řádku kusovníku, který je k dispozici v návrháři kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="3e3d8-145">Volitelně můžete pro vyměněný objekt vystavit fakturu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="3e3d8-146">Jestliže vytvoříte řádek servisní zakázky, můžete pro vyměněnou součást vystavit fakturu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="3e3d8-147">Pokud pro výměnu nevytvoříte řádek servisní zakázky, uchovají se pro vaše záznamy informace o výměně a sleduje se historie předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="3e3d8-148">Změna způsobu zobrazení informací na řádku Kusovníku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="3e3d8-149">Pro všechny kusovníky šablon a servisní kusovníky můžete určit, jakým způsobem se mají zobrazovat informace z řádků kusovníků.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="3e3d8-150">Tyto změny se vztahují na všechny kusovníky šablony a kusovníky servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="3e3d8-151">Patří sem ty, které jsou připojeny k předmětům servisu.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="3e3d8-152">Nastavení číselných řad pro kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="3e3d8-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="3e3d8-153">Chcete-li používat kusovníky šablony, je nutné nastavit dvě číselné řady.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="3e3d8-154">Jedna řada je určená pro kusovník šablony a druhá pro číslování řádků historie kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3e3d8-155">Číselné řady se používají k přidělování identifikátorů k záznamům, které je vyžadují.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="3e3d8-156">Aby bylo možné přiřadit číselnou řadu pro Kusovník šablony nebo číslo řádku historie Kusovníku, musíte nastavit kódy číselných řad.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="3e3d8-157">Nastavit číselné řady</span><span class="sxs-lookup"><span data-stu-id="3e3d8-157">Set up number sequences</span></span>

1.  <span data-ttu-id="3e3d8-158">Na stránce se seznamem **číselné řady** vytvořte číselné řady pro kusovníky šablony a čísla řádků historie Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="3e3d8-159">Klikněte **Správa servisu** \> **Nastavení** \> **Parametry správy servisu**.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="3e3d8-160">Klepněte na tlačítko **číselné řady** a vyberte kód číselné řady pro reference číselné řady, které jste vytvořili ve formuláři **číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="3e3d8-161">Uložte změny zavřením formuláře.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3e3d8-162">Číslo řádku historie Kusovníku používá systém k přidružení transakcí v historii Kusovníku k servisní smlouvě nebo servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="3e3d8-163">Číslo řádku historie kusovníku se nezobrazuje v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="3e3d8-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="3e3d8-164">Viz také</span><span class="sxs-lookup"><span data-stu-id="3e3d8-164">See also</span></span>

[<span data-ttu-id="3e3d8-165">Vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="3e3d8-166">Správa šablon kusovníku pro vztahy předmětu</span><span class="sxs-lookup"><span data-stu-id="3e3d8-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="3e3d8-167">Změna servisního kusovníku</span><span class="sxs-lookup"><span data-stu-id="3e3d8-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]