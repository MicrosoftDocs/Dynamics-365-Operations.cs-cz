---
title: Vytvoření vlastních polí a práce s nimi
description: Toto téma popisuje, jak v uživatelském rozhraní vytvářet vlastní pole pro přizpůsobení aplikace vašemu podnikání.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f689bb3ec844459d1dd6e199804a30f3e0cb38bc
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112329"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="749ba-103">Vytvoření vlastních polí a práce s nimi</span><span class="sxs-lookup"><span data-stu-id="749ba-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="749ba-104">Aplikace sice poskytuje rozsáhlou škálu standardních polí pro správu širokého rozsahu obchodních procesů. Někdy však společnost potřebuje sledovat ve svém systému i další informace.</span><span class="sxs-lookup"><span data-stu-id="749ba-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="749ba-105">Zatímco programátoři mohou tato pole přidat jako rozšíření ve vývojářských nástrojích, funkce vlastních polí umožňuje přidávat pole přímo z uživatelského rozhraní, což vám umožní přizpůsobit aplikaci tak, aby vyhovovala vašemu podniku pomocí webového prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="749ba-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="749ba-106">Možnost přidat vlastní pole je k dispozici v aktualizaci platform update 13 a novější.</span><span class="sxs-lookup"><span data-stu-id="749ba-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="749ba-107">K této funkci mají přístup pouze uživatelé se zvláštními oprávněními.</span><span class="sxs-lookup"><span data-stu-id="749ba-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="749ba-108">Toto video ukazuje, jak je snadné přidat na stránku vlastní pole: [Přidávání vlastních polí](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="749ba-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="749ba-109">Vytváření vlastních polí</span><span class="sxs-lookup"><span data-stu-id="749ba-109">Creating custom fields</span></span>

<span data-ttu-id="749ba-110">Poté, co jste identifikovali doplňující informace, které chcete v aplikaci sledovat, můžete vytvořit vlastní pole v příslušné tabulce a vystavit toto nové pole na stránce.</span><span class="sxs-lookup"><span data-stu-id="749ba-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="749ba-111">Proces vytváření vlastního pole a umístění daného pole ve formuláři je popsán v následujících krocích.</span><span class="sxs-lookup"><span data-stu-id="749ba-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="749ba-112">Přejděte na formulář, ve kterém chcete mít nové pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="749ba-113">Vzhledem k tomu, že cílem je mít vlastní pole ve formuláři, vstupní bod pro vytváření vlastního pole existuje v rámci infividuálního nastavení.</span><span class="sxs-lookup"><span data-stu-id="749ba-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="749ba-114">Otevřete panel nástrojů individuálního nastavení výběrem položky **Možnosti**a pak **Přizpůsobit tento formulář**.</span><span class="sxs-lookup"><span data-stu-id="749ba-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="749ba-115">Klikněte na **Vložit** a pak **Pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="749ba-116">Vyberte oblast formuláře, ve kterém chcete zveřejnit nové pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="749ba-117">Po výběru možnosti **Vložit pole** zobrazí dialogové okno seznam existujících polí, která lze vložit do vybrané oblasti formuláře.</span><span class="sxs-lookup"><span data-stu-id="749ba-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="749ba-118">Ověřte, že pole, které vás zajímá, již v seznamu neexistuje.</span><span class="sxs-lookup"><span data-stu-id="749ba-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="749ba-119">Pokud ano, můžete jednoduše toto pole vybrat v seznamu a kliknout na **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="749ba-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="749ba-120">Klikněte na tlačítko **Vytvořit nové pole** nad seznamem a zahájíte proces vytváření vlastního pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="749ba-121">Otevře se dialogové okno **Vytvořit nové pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="749ba-122">Pokud se nezobrazí tlačítko **Vytvořit nové pole**, nemáte potřebná oprávnění k použití této funkce.</span><span class="sxs-lookup"><span data-stu-id="749ba-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="749ba-123">V dialogovém okně **Vytvořit nové pole** zadejte následující informace.</span><span class="sxs-lookup"><span data-stu-id="749ba-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="749ba-124">Vyberte databázovou tabulku, do které chcete přidat toto pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="749ba-125">Všimněte si, že v rozevíracím seznamu se zobrazí pouze tabulky, které podporují vlastní pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="749ba-126">Technické podrobnosti týkající se podporovaných tabulek jsou uvedený v následující části.</span><span class="sxs-lookup"><span data-stu-id="749ba-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="749ba-127">Zvolte zyp dat pro nové pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-127">Select the data type for the new field.</span></span> <span data-ttu-id="749ba-128">Dostupné datové typy jsou zaškrtávací políčko, datum, datum a čas, desetinné číslo, číslo, rozevírací seznam a text.</span><span class="sxs-lookup"><span data-stu-id="749ba-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="749ba-129">Pokud vyberet datový typ text, můžete také určit maximální délka textu, který lze zadat do tohoto pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="749ba-130">Pokud zvolíte typ dat rozevírací seznam, můžete také vybrat sadu platných hodnot pro toto pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="749ba-131">Zadejte název, popisek a text nápovědy pro dané pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="749ba-132">Název odpovídá názvu fyzickému názvu pole v databázi, zatímco popisek a text nápovědy jsou texty představující toto pole v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="749ba-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="749ba-133">Pokud se jedná o jediné pole, které chcete vytvořit pro tento formulář, klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="749ba-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="749ba-134">Pokud chcete vytvořit další pole, klikněte na tlačítko **Uložit a nový** a pokračujte opět krokem 7.</span><span class="sxs-lookup"><span data-stu-id="749ba-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="749ba-135">Pamatujte, že v současnosti existuje limit **20 vlastních polí pro tabulku**.</span><span class="sxs-lookup"><span data-stu-id="749ba-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="749ba-136">Opuštěním dialogového okna **Vytvořit nové pole** se vrátíte do dialogového okna **Vložit pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="749ba-137">Všechna právě přidaná vlastní pole budou automaticky označena v seznamu polí, která budou vložena do formuláře.</span><span class="sxs-lookup"><span data-stu-id="749ba-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="749ba-138">Klikněte na tlačítko **Vložit** a vložíte označená pole do vybrané oblasti formuláře.</span><span class="sxs-lookup"><span data-stu-id="749ba-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="749ba-139">**Volitelné:** Povolte režim **Přesunout** z panelu nástrojů individuálního nastavení a přesuňte nová pole na požadované místo ve vybrané oblasti.</span><span class="sxs-lookup"><span data-stu-id="749ba-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="749ba-140">Další informace o použití různých funkcí individuálního nastavení za účelem optimalizace formuláře pro vaše osobní použití naleznete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="749ba-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="749ba-141">Sdílení vlastních polí s dalšími uživateli</span><span class="sxs-lookup"><span data-stu-id="749ba-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="749ba-142">Po vytvoření vlastního pole a jeho vystavení ve formuláři můžete chtít poskytnout toto aktualizované zobrazení stránky s novým polem jiným uživatelům v systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="749ba-143">Toho lze dosáhnout dvěma různými způsoby pomocí možností individuálního nastavení produktu:</span><span class="sxs-lookup"><span data-stu-id="749ba-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="749ba-144">Doporučený postup je prostřednictvím správce systému, který může individuální nastavení předat všem uživatelům nebo podmnožině uživatelů.</span><span class="sxs-lookup"><span data-stu-id="749ba-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="749ba-145">Další informace najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="749ba-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="749ba-146">Případně můžete exportovat své změny (nazývané *individuální nastavení*), zaslat je jednomu nebo více uživatelům a nechat tyto jednotlivé uživatelé importovat vaše změny.</span><span class="sxs-lookup"><span data-stu-id="749ba-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="749ba-147">Možnost **Spravovat** na panelu nástrojů induviduálního nastavení vám umožní exportovat a importovat individuální nastavení.</span><span class="sxs-lookup"><span data-stu-id="749ba-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="749ba-148">Správa vlastních polí</span><span class="sxs-lookup"><span data-stu-id="749ba-148">Managing custom fields</span></span>

<span data-ttu-id="749ba-149">Správu všech vlastních polí v systému lze provádět pomocí stránky **Vlastní pole** v modulu Správa systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="749ba-150">Tato stránku umožňuje uživatelům přístup k mnoha možnostem, včetně:</span><span class="sxs-lookup"><span data-stu-id="749ba-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="749ba-151">Zobrazení seznamu všech vlastních polí v systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="749ba-152">Omezené úpravy existujících vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="749ba-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="749ba-153">Odstranění vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="749ba-153">Deleting custom fields.</span></span>
- <span data-ttu-id="749ba-154">Vystavení vlastních polí na datových entitách.</span><span class="sxs-lookup"><span data-stu-id="749ba-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="749ba-155">Poskytnutí překladů popisků vlastních polí a textu nápovědy.</span><span class="sxs-lookup"><span data-stu-id="749ba-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="749ba-156">Zobrazení všech vlastních polí</span><span class="sxs-lookup"><span data-stu-id="749ba-156">Viewing all custom fields</span></span>

<span data-ttu-id="749ba-157">Stránka **Vlastní pole** poskytuje zobrazení všech vlastních polí, která bylá definována v systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="749ba-158">Jednoduše vyberte tabulku, která vás zajímá, a stránka se zaktualizuje a zobrazí seznam vlastních polí přidružených k tabulce.</span><span class="sxs-lookup"><span data-stu-id="749ba-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="749ba-159">Výběr vlastního pole ze seznamu vám umožní zobrazit všechny podrobnosti o poli.</span><span class="sxs-lookup"><span data-stu-id="749ba-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="749ba-160">Úprava vlastních polí</span><span class="sxs-lookup"><span data-stu-id="749ba-160">Editing custom fields</span></span>

<span data-ttu-id="749ba-161">Po vytvoření vlastního pole lze upravit pouze určité části informací o vlastních polích na stránce **Vlastní pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="749ba-162">*Můžete* změnit tyto atributy:</span><span class="sxs-lookup"><span data-stu-id="749ba-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="749ba-163">Popisek</span><span class="sxs-lookup"><span data-stu-id="749ba-163">Label</span></span>
- <span data-ttu-id="749ba-164">Text nápovědy</span><span class="sxs-lookup"><span data-stu-id="749ba-164">Help text</span></span>
- <span data-ttu-id="749ba-165">Délka textových polí</span><span class="sxs-lookup"><span data-stu-id="749ba-165">Length, for Text fields</span></span>

<span data-ttu-id="749ba-166">*Nemůžete* upravit následující atributy:</span><span class="sxs-lookup"><span data-stu-id="749ba-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="749ba-167">Název pole</span><span class="sxs-lookup"><span data-stu-id="749ba-167">Field name</span></span>
- <span data-ttu-id="749ba-168">Datový typ</span><span class="sxs-lookup"><span data-stu-id="749ba-168">Data type</span></span>

<span data-ttu-id="749ba-169">Pro rozevírací seznam polí lze také změnit uspořádání sady platných hodnot pro vlastní pole a přidat nové hodnoty. Nicméně existující hodnoty rozevíracího seznamu polí nelze odebrat.</span><span class="sxs-lookup"><span data-stu-id="749ba-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="749ba-170">Nezapomeňte kliknout na **Použít změny** po dokončení úprav polí pro určitou tabulku, aby se změny uložily.</span><span class="sxs-lookup"><span data-stu-id="749ba-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="749ba-171">Vystavení vlastních polí na datových entitách</span><span class="sxs-lookup"><span data-stu-id="749ba-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="749ba-172">Je rovněž důležité umožnit, aby byla vlastní pole viditelná na datových entitách.</span><span class="sxs-lookup"><span data-stu-id="749ba-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="749ba-173">Datové entity se používají ve funkci [Přehled integrace Office](../../dev-itpro/office-integration/office-integration.md), stejně jako u scénáře importu a exportu dat.</span><span class="sxs-lookup"><span data-stu-id="749ba-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="749ba-174">Pro vystavení vlastního pole na datové entitě postupujte podle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="749ba-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="749ba-175">Vyberte vlastní pole ve formuláři **Vlastní pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="749ba-176">Rozbalte část **Entity** a zobrazte sadu příslušných entit.</span><span class="sxs-lookup"><span data-stu-id="749ba-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="749ba-177">Klikněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="749ba-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="749ba-178">Změňte pole **Povoleno**, které má být vybráno pro každou entitu, která vystaví toto pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="749ba-179">Kliknutím na tlačítko **Použít změny** uložte své volby.</span><span class="sxs-lookup"><span data-stu-id="749ba-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="749ba-180">Povolení zobrazení vlastních polí v jiných jazycích</span><span class="sxs-lookup"><span data-stu-id="749ba-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="749ba-181">Vzhledem k tomu, že vlastní pole mohou být vyžadována v různých jazycích, poskytuje stránka **Vlastní pole** mechanismus, který umožní překlad popisku a textu nápovědy vlastního pole do dalších jazyků.</span><span class="sxs-lookup"><span data-stu-id="749ba-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="749ba-182">Následující kroky popisují proces překladu vlastních polí do jiných jazyků:</span><span class="sxs-lookup"><span data-stu-id="749ba-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="749ba-183">Vyberte vlastní pole na stránce **Vlastní pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="749ba-184">Výběr tlačítko **Překlady** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="749ba-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="749ba-185">Otevře se rozevírací nabídka s existujícími překlady pro toto pole.</span><span class="sxs-lookup"><span data-stu-id="749ba-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="749ba-186">Rozevírací nabídka **Jazyk** zobrazuje sadu jazyků, pro které již byly poskytnuty překlady.</span><span class="sxs-lookup"><span data-stu-id="749ba-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="749ba-187">Pokud chcete upravit stávající překlad, z nabídky vyberte požadovaný jazyk a upravte hodnoty pro popisek a text nápovědy.</span><span class="sxs-lookup"><span data-stu-id="749ba-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="749ba-188">V opačném případě klikněte natlačítko **Přidat jazyk**, vyberte požadovaný jazyk z nabídky a potom zadejte přeložené hodnoty pro popisek a text nápovědy.</span><span class="sxs-lookup"><span data-stu-id="749ba-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="749ba-189">Po dokončení klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="749ba-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="749ba-190">Odstranění vlastních polí</span><span class="sxs-lookup"><span data-stu-id="749ba-190">Deleting custom fields</span></span>

<span data-ttu-id="749ba-191">Ve výjimečných případech se můžete rozhodnout, že vlastní pole již není potřeba.</span><span class="sxs-lookup"><span data-stu-id="749ba-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="749ba-192">V takovém případě může správce systému odstranit pole ze stránky **Vlastní pole**.</span><span class="sxs-lookup"><span data-stu-id="749ba-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="749ba-193">Je třeba vybrat správné pole, kliknout na **Odstranit**, kliknout na **Ano** pro potvrzení odstranění a nakonec kliknout na tlačítko **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="749ba-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="749ba-194">Tuto akci nelze vrátit zpět a výsledkem bude, že data spojená s polem budou natrvalo odstraněna z databáze.</span><span class="sxs-lookup"><span data-stu-id="749ba-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="749ba-195">Dodatek</span><span class="sxs-lookup"><span data-stu-id="749ba-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="749ba-196">Kdo může vytvářet vlastní pole?</span><span class="sxs-lookup"><span data-stu-id="749ba-196">Who can create custom fields?</span></span>

<span data-ttu-id="749ba-197">Jako ochranné opatření je ve výchozím nastavení umožněno vytváření vlastních polí pouze správcům systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="749ba-198">Nicméně uživatelům typu power user, které určí organizace, mohou být přidělena práva k vytváření vlastních polí od správce systému pomocí role zabezpečení **Uživatel power user přizpůsobení runtime**.</span><span class="sxs-lookup"><span data-stu-id="749ba-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="749ba-199">Uživatelé bez této role zabezpečení nebudete moci vytvářet vlastní pole, ale stále budou moci zobrazit nebo používat vlastní pole přidaná ostatními uživateli v systému.</span><span class="sxs-lookup"><span data-stu-id="749ba-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="749ba-200">Jaké tabulky podporují vlastní pole?</span><span class="sxs-lookup"><span data-stu-id="749ba-200">What tables support custom fields?</span></span>

<span data-ttu-id="749ba-201">Z důvodů výkonnosti a z technických důvodů momentálně podporují přidání vlastních polí pouze tabulky splňující následující podmínky.</span><span class="sxs-lookup"><span data-stu-id="749ba-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="749ba-202">Tabulka musí být označena jako jedna z těchto skupin:</span><span class="sxs-lookup"><span data-stu-id="749ba-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="749ba-203">Seskupit</span><span class="sxs-lookup"><span data-stu-id="749ba-203">Group</span></span>
    - <span data-ttu-id="749ba-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="749ba-204">WorksheetHeader</span></span>
    - <span data-ttu-id="749ba-205">Hlavní</span><span class="sxs-lookup"><span data-stu-id="749ba-205">Main</span></span>
    - <span data-ttu-id="749ba-206">Různé</span><span class="sxs-lookup"><span data-stu-id="749ba-206">Miscellaneous</span></span>
    - <span data-ttu-id="749ba-207">Parametr</span><span class="sxs-lookup"><span data-stu-id="749ba-207">Parameter</span></span>
    - <span data-ttu-id="749ba-208">Odkaz</span><span class="sxs-lookup"><span data-stu-id="749ba-208">Reference</span></span>
    - <span data-ttu-id="749ba-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="749ba-209">TransactionHeader</span></span>

- <span data-ttu-id="749ba-210">Tabulka nemůže rozšiřovat jinou tabulku.</span><span class="sxs-lookup"><span data-stu-id="749ba-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="749ba-211">Tabulka nemůže být označena jako systémová tabulka.</span><span class="sxs-lookup"><span data-stu-id="749ba-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="749ba-212">Tabulka nemůže být dočasná.</span><span class="sxs-lookup"><span data-stu-id="749ba-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="749ba-213">Lze odkazovat na vlastní pole z nástrojů pro vývojáře?</span><span class="sxs-lookup"><span data-stu-id="749ba-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="749ba-214">Vlastní pole lze spravovat pouze prostřednictvím uživatelského rozhraní a nelze na ně odkazovat pomocí kódu.</span><span class="sxs-lookup"><span data-stu-id="749ba-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
