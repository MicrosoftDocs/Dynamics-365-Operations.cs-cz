---
title: Otevření šablon finančního deníku v aplikaci Office
description: Toto téma popisuje problémy, které mohou nastat při vytváření vlastních finančních deníků pomocí šablony Microsoft Excel.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089450"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="13aa0-103">Otevření šablon finančního deníku v aplikaci Office</span><span class="sxs-lookup"><span data-stu-id="13aa0-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13aa0-104">Toto téma popisuje problémy, které mohou nastat při vytváření vlastních finančních deníků pomocí šablony Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="13aa0-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="13aa0-105">Příznak</span><span class="sxs-lookup"><span data-stu-id="13aa0-105">Symptom</span></span>

<span data-ttu-id="13aa0-106">Vytvořili jste vlastní šablonu aplikace Excel pro finanční deníky, ale ta se nezobrazuje v nabídce **Otevřít řádky v aplikaci Excel**.</span><span class="sxs-lookup"><span data-stu-id="13aa0-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="13aa0-107">Případně se v nabídce objeví, ale po výběru se otevře jiná šablona.</span><span class="sxs-lookup"><span data-stu-id="13aa0-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="13aa0-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="13aa0-108">Resolution</span></span>

<span data-ttu-id="13aa0-109">Výchozí funkce Otevřít v aplikaci Excel používá kořenový zdroj dat (tabulku) aktuální stránky k určení, které šablony Office nebo datové entity se zobrazí jako možnosti v nabídce **Otevřít v aplikaci Excel**.</span><span class="sxs-lookup"><span data-stu-id="13aa0-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="13aa0-110">Toto chování není ideální, protože finanční deníky používají stejné tabulky (LedgerJournalTable a LedgerJournalTrans) jako kořenový zdroj dat mnoha jiných typů deníků.</span><span class="sxs-lookup"><span data-stu-id="13aa0-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="13aa0-111">V případě finančních deníků je funkce Otevřít řádky v aplikaci Excel určena k zobrazení šablon, které jsou určeny pro deník, s nímž právě pracujete (např. pro finanční deník nebo deník plateb).</span><span class="sxs-lookup"><span data-stu-id="13aa0-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="13aa0-112">Například šablona, která je určena k použití s deníkem plateb dodavatele, bude navržena tak, aby vynucovala váš primární účet jako účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="13aa0-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="13aa0-113">Pokud chcete zvýšit úroveň šablony tak, aby byla k dispozici v nabídkách **Otevřít řádky v aplikaci Excel** a **Otevřít v aplikaci Excel**, jednoduchou možností pro vývojáře je implementace rozhraní **LedgerIJournalExcelTemplate** a rozšíření třídy **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="13aa0-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="13aa0-114">V systému je implementováno mnoho příkladů tohoto přístupu.</span><span class="sxs-lookup"><span data-stu-id="13aa0-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="13aa0-115">Jedním příkladem, který lze použít jako referenci, je rozhraní **LedgerDailyJournalExcelTemplate**, které bylo vytvořeno pro finanční deník (nebo denní deník).</span><span class="sxs-lookup"><span data-stu-id="13aa0-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="13aa0-116">Když je pro vaši šablonu implementováno rozhraní **LedgerIJournalExcelTemplate**, nabídka **Otevřít řádky v aplikaci Excel** filtruje šablony podle typu vašeho deníku a zobrazí pouze šablony, které jsou pro daný deník k dispozici.</span><span class="sxs-lookup"><span data-stu-id="13aa0-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="13aa0-117">Rozhraní také poskytuje metodu ověření, která zajišťuje, že šablonu nelze otevřít pro deník, pokud nesplňuje požadavky na typ účtu.</span><span class="sxs-lookup"><span data-stu-id="13aa0-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="13aa0-118">Můžete například určit, že typ účtu musí být **Dodavatel** nebo **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="13aa0-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="13aa0-119">Další informace o této funkci najdete v části [Přidejte šablony do nabídky Otevřít řádky v aplikaci Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="13aa0-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
