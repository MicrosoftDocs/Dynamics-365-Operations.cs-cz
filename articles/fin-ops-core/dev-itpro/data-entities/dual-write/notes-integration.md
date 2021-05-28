---
title: Integrace poznámek
description: Toto téma popisuje integraci dat poznámek v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ed068f4264269334babec9acd59d9d58551333b4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018379"
---
# <a name="note-integration"></a><span data-ttu-id="44517-103">Integrace poznámek</span><span class="sxs-lookup"><span data-stu-id="44517-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="44517-104">Během obchodních procesů Microsoft Dynamics 365 uživatelé často shromažďují informace o svých zákaznících.</span><span class="sxs-lookup"><span data-stu-id="44517-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="44517-105">Tyto informace se zaznamenávají jako aktivity a poznámky.</span><span class="sxs-lookup"><span data-stu-id="44517-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="44517-106">Toto téma popisuje integraci dat poznámek v duálním zápisu.</span><span class="sxs-lookup"><span data-stu-id="44517-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="44517-107">Informace o zákaznících lze klasifikovat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="44517-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="44517-108">**Akční informace, které uživatel Dynamics 365 zpracovává jménem zákazníka** – Například společnost Contoso (uživatel Dynamics 365) pořádá televizní soutěž.</span><span class="sxs-lookup"><span data-stu-id="44517-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="44517-109">Jeden ze zákazníků společnosti Contoso (zákazník) se chce televizní soutěže zúčastnit.</span><span class="sxs-lookup"><span data-stu-id="44517-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="44517-110">Zákazník požádá zaměstnance společnosti Contoso, aby mu rezervoval slot v televizní soutěži.</span><span class="sxs-lookup"><span data-stu-id="44517-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="44517-111">Rezervace probíhá v kalendáři účastníka akce společnosti Contoso.</span><span class="sxs-lookup"><span data-stu-id="44517-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="44517-112">**Akční informace pro uživatele Dynamics 365** – Například zákazník, který kupuje jednotku Surface, zadá speciální pokyny, které označují, že by zařízení mělo být před dodáním zabaleno v dárkovém balení.</span><span class="sxs-lookup"><span data-stu-id="44517-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="44517-113">Tyto pokyny jsou akční informace, s nimiž by měl zacházet zaměstnanec společnosti Contoso odpovědný za balení.</span><span class="sxs-lookup"><span data-stu-id="44517-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="44517-114">**Neakční informace** – Například zákazník navštíví obchod Contoso a během rozhovoru se spolupracovníkem obchodu projeví zájem o hry a herní příslušenství *Halo*.</span><span class="sxs-lookup"><span data-stu-id="44517-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="44517-115">Obchodník si tyto informace poznamená.</span><span class="sxs-lookup"><span data-stu-id="44517-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="44517-116">Nástroj pro doporučení produktu jej poté použije k doporučení zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="44517-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="44517-117">Obecně jsou akční informace zachyceny jako *činnosti* v aplikacích Finance and Operations a aplikacích Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="44517-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="44517-118">Neakční jsou informace zachyceny jako *poznámky* v aplikacích Finance and Operations a *anotace* v aplikacích Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="44517-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="44517-119">Ačkoli poznámky jsou určeny pro neaktivní informace, aplikace vám nebudou bránit v jejich použití k ukládání a zpracovávání akčních informací, pokud je chcete použít tímto způsobem.</span><span class="sxs-lookup"><span data-stu-id="44517-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="44517-120">Společnost Microsoft v současné době vydává funkce pro integraci poznámek.</span><span class="sxs-lookup"><span data-stu-id="44517-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="44517-121">(Funkce pro integraci aktivit bude uvolněna později.) Integrace poznámek je k dispozici pro zákazníky, dodavatele, prodejní objednávky a nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="44517-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="44517-122">Vytvoření poznámky v aplikaci Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="44517-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="44517-123">Chcete-li vytvořit poznámku v aplikaci Customer Engagement a poté ji synchronizovat do aplikace Finance and Operations, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="44517-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="44517-124">V aplikaci Customer Engagement otevřete záznam účtu pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="44517-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="44517-125">V podokně **Časová osa** vyberte znaménko plus (**+**) a poté vyberte **Poznámka** k vytvoření poznámky.</span><span class="sxs-lookup"><span data-stu-id="44517-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Vytvoření poznámky v aplikaci Customer Engagement](media/notes-ce-1.png)

3. <span data-ttu-id="44517-127">Zadejte název a popis a poté vyberte **Přidat poznámku**.</span><span class="sxs-lookup"><span data-stu-id="44517-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Zadání nadpisu a popisu](media/notes-ce-2.png)

    <span data-ttu-id="44517-129">Nová poznámka se přidá na časovou osu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="44517-129">The new note is added to the customer timeline.</span></span>

    ![Nová poznámka na časové ose zákazníka](media/notes-ce-3.png)

4. <span data-ttu-id="44517-131">Přihlaste se do aplikace Finance and Operations a otevřete stejný záznam zákazníka.</span><span class="sxs-lookup"><span data-stu-id="44517-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="44517-132">Všimněte si, že tlačítko **Přílohy** (symbol kancelářské sponky) v pravém horním rohu označuje, že záznam má přílohu.</span><span class="sxs-lookup"><span data-stu-id="44517-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Oznámení o příloze](media/notes-ce-4.png)

5. <span data-ttu-id="44517-134">Vyberte tlačítko **Přílohy** pro otevření stránky **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="44517-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="44517-135">Měli byste najít poznámku, kterou jste vytvořili v aplikaci Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="44517-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Poznámka z aplikace Customer Engagement](media/notes-ce-5.png)

<span data-ttu-id="44517-137">Všechny aktualizace poznámky se synchronizují tam a zpět mezi aplikací Finance and Operations a aplikací Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="44517-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="44517-138">Vytvoření poznámky v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="44517-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="44517-139">Poznámku můžete vytvořit také v aplikaci Finance and Operations a poté ji synchronizovat do aplikace Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="44517-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="44517-140">Chcete-li vytvořit poznámku v aplikaci Finance and Operations a poté ji synchronizovat do aplikace Customer Engagement, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="44517-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="44517-141">V aplikaci Finance and Operations na stránce **Přílohy** vyberte **Nový** \> **Poznámka**.</span><span class="sxs-lookup"><span data-stu-id="44517-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Vytvoření poznámky v aplikaci Finance and Operations](media/notes-fo-1.png)

2. <span data-ttu-id="44517-143">Zadejte název a krátkou sadu pokynů a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="44517-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Zadání nadpisu a pokynů](media/notes-fo-2.png)

3. <span data-ttu-id="44517-145">V aplikaci Customer Engagement aktualizujte záznam.</span><span class="sxs-lookup"><span data-stu-id="44517-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="44517-146">Na časové ose byste měli najít novou poznámku.</span><span class="sxs-lookup"><span data-stu-id="44517-146">You should find the new note on the timeline.</span></span>

    ![Nová poznámka na časové ose v aplikaci Customer Engagement](media/notes-fo-3.png)

<span data-ttu-id="44517-148">Poznámku můžete klasifikovat jako interní nebo externí.</span><span class="sxs-lookup"><span data-stu-id="44517-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="44517-149">V aplikaci Finance and Operations na stránce **Přílohy** otevřete poznámku a poté v poli **Omezení** vyberte **Interní**, nebo **Externí**.</span><span class="sxs-lookup"><span data-stu-id="44517-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Pole omezení](media/notes-fo-4.png)

<span data-ttu-id="44517-151">Můžete také vytvořit adresu URL.</span><span class="sxs-lookup"><span data-stu-id="44517-151">You can also create a URL.</span></span>

1. <span data-ttu-id="44517-152">V aplikaci Finance and Operations na stránce **Přílohy** vyberte **Nový** \> **Adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="44517-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="44517-153">Zadejte nadpis a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="44517-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="44517-154">V poli **Omezení** pole, vyberte **Interní**, nebo **Externí**.</span><span class="sxs-lookup"><span data-stu-id="44517-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Vytvoření adresy URL v aplikaci Finance and Operations](media/notes-fo-5.png)

4. <span data-ttu-id="44517-156">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="44517-156">Select **Save**.</span></span>

    <span data-ttu-id="44517-157">Protože aplikace Customer Engagement nemají typ adresy URL, je adresa URL integrována s duálním zápisem jako poznámka.</span><span class="sxs-lookup"><span data-stu-id="44517-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Adresa URL zobrazená jako poznámka v aplikaci Customer Engagement](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="44517-159">Přílohy souborů nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="44517-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="44517-160">Šablony</span><span class="sxs-lookup"><span data-stu-id="44517-160">Templates</span></span>

<span data-ttu-id="44517-161">Integrace poznámek zahrnuje mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="44517-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="44517-162">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="44517-162">Finance and Operations app</span></span> | <span data-ttu-id="44517-163">Aplikace Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="44517-163">Customer engagement app</span></span> | <span data-ttu-id="44517-164">popis</span><span class="sxs-lookup"><span data-stu-id="44517-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="44517-165">Přílohy zákazníků</span><span class="sxs-lookup"><span data-stu-id="44517-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="44517-166">Poznámky</span><span class="sxs-lookup"><span data-stu-id="44517-166">Annotations</span></span> | <span data-ttu-id="44517-167">Firmy, které používají prostý text a adresy URL k zachycení specifických informací o zákazníkovi (pro organizace i osoby).</span><span class="sxs-lookup"><span data-stu-id="44517-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="44517-168">Přílohy dokumentu dodavatele</span><span class="sxs-lookup"><span data-stu-id="44517-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="44517-169">Poznámky</span><span class="sxs-lookup"><span data-stu-id="44517-169">Annotations</span></span> | <span data-ttu-id="44517-170">Firmy, které používají prostý text a adresy URL k zachycení specifických informací o dodavateli (pro organizace i osoby).</span><span class="sxs-lookup"><span data-stu-id="44517-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="44517-171">Přílohy dokumentu záhlaví prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="44517-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="44517-172">Poznámky</span><span class="sxs-lookup"><span data-stu-id="44517-172">Annotations</span></span> | <span data-ttu-id="44517-173">Firmy, které používají k zachycení konkrétních informací o prodejní objednávce prostý text a adresy URL.</span><span class="sxs-lookup"><span data-stu-id="44517-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="44517-174">Přílohy dokumentu záhlaví nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="44517-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="44517-175">Poznámky</span><span class="sxs-lookup"><span data-stu-id="44517-175">Annotations</span></span> | <span data-ttu-id="44517-176">Firmy, které používají k zachycení konkrétních informací o nákupní objednávce prostý text a adresy URL.</span><span class="sxs-lookup"><span data-stu-id="44517-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="44517-177">Další informace viz [Odkaz na mapování duálního zápisu ](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="44517-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
