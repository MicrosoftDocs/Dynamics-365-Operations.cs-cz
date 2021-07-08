---
title: Časté otázky týkající se resetování datového tržiště
description: Toto téma poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266602"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="9fecf-103">Časté otázky týkající se resetování datového tržiště</span><span class="sxs-lookup"><span data-stu-id="9fecf-103">Data mart resets FAQ</span></span>

<span data-ttu-id="9fecf-104">Toto téma poskytuje odpovědi na několik dotazů týkajících se resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fecf-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="9fecf-105">Reset datového tržiště může být časově náročný proces a v závislosti na okolnostech nemusí být požadovaným řešením.</span><span class="sxs-lookup"><span data-stu-id="9fecf-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="9fecf-106">Toto téma proto zahrnuje informace o okolnostech, kdy může pomoci reset datového tržiště, a také o okolnostech, kdy je nepravděpodobné, že by to pomohlo.</span><span class="sxs-lookup"><span data-stu-id="9fecf-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="9fecf-107">Co je resetování datového tržiště?</span><span class="sxs-lookup"><span data-stu-id="9fecf-107">What is a data mart reset?</span></span>

<span data-ttu-id="9fecf-108">Reset datového tržiště deaktivuje úlohy integrace, odstraní všechna data datového tržiště a poté znovu povolí integraci.</span><span class="sxs-lookup"><span data-stu-id="9fecf-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="9fecf-109">Aby bylo zajištěno, že nebudou vložena stará data, lze reset datového tržiště spustit až po dokončení stávajících úkolů.</span><span class="sxs-lookup"><span data-stu-id="9fecf-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="9fecf-110">Pokud se pokusíte resetovat datové tržiště před dokončením všech úkolů, může se zobrazit zpráva jako: „Obnovení datového tržiště nebylo možné zpracovat z důvodu aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="9fecf-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="9fecf-111">Prosím zkuste to znovu později.“</span><span class="sxs-lookup"><span data-stu-id="9fecf-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="9fecf-112">Kdy je třeba provést reset datového tržiště?</span><span class="sxs-lookup"><span data-stu-id="9fecf-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="9fecf-113">Pokud se na vaši situaci vztahuje jeden nebo více z následujících výroků, může vaše organizace těžit z resetování datového tržiště:</span><span class="sxs-lookup"><span data-stu-id="9fecf-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="9fecf-114">Byla obnovena databáze aplikací.</span><span class="sxs-lookup"><span data-stu-id="9fecf-114">The application database was restored.</span></span>
- <span data-ttu-id="9fecf-115">Otevřeli jste lístek podpory a technik podpory vám nařídil resetovat datové tržiště jako součást kroku odstraňování problémů.</span><span class="sxs-lookup"><span data-stu-id="9fecf-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="9fecf-116">Kdy není resetování datového tržiště vhodné?</span><span class="sxs-lookup"><span data-stu-id="9fecf-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="9fecf-117">Zde jsou některé okolnosti, kdy nedoporučujeme resetovat datové tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fecf-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="9fecf-118">Máte problémy s výkonem spojené se synchronizací dat.</span><span class="sxs-lookup"><span data-stu-id="9fecf-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="9fecf-119">Máte opakující se vzor pro resetování z některého z následujících důvodů:</span><span class="sxs-lookup"><span data-stu-id="9fecf-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="9fecf-120">**Chybějící data** - Pokud si všimnete, že data chybí, otevřete si u Microsoftu lístek podpory a zkontrolujte formát zprávy a možné problémy se synchronizací dat.</span><span class="sxs-lookup"><span data-stu-id="9fecf-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="9fecf-121">**Zaseknutý stav integrace**</span><span class="sxs-lookup"><span data-stu-id="9fecf-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="9fecf-122">**Zastaralé záznamy** - Zastaralé záznamy samy o sobě nutně neospravedlňují resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fecf-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="9fecf-123">Pokud máte velkou datovou sadu, proces resetování bude nějakou dobu trvat, ale je nepravděpodobné, že by vedl ke zlepšení.</span><span class="sxs-lookup"><span data-stu-id="9fecf-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="9fecf-124">Pokud resetuji datové tržiště, přijdu o sestavy, které jsem již vytvořil?</span><span class="sxs-lookup"><span data-stu-id="9fecf-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="9fecf-125">Ne.</span><span class="sxs-lookup"><span data-stu-id="9fecf-125">No.</span></span> <span data-ttu-id="9fecf-126">Vaše sestavy jsou uloženy v tabulkách SQL, které nejsou ovlivněny resetem datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fecf-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="9fecf-127">Pokud se obáváte ztráty jakýchkoli sestav, které jste navrhli, můžete zálohovat návrhy, které nechcete ztratit.</span><span class="sxs-lookup"><span data-stu-id="9fecf-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="9fecf-128">Chcete-li zálohovat návrhy, otevřete návrhář sestav a přejděte na **Společnost \> Společnosti \> Stavební bloky \> Export**.</span><span class="sxs-lookup"><span data-stu-id="9fecf-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="9fecf-129">Musí všichni uživatelé opustit systém, než budu moci resetovat datový trh?</span><span class="sxs-lookup"><span data-stu-id="9fecf-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="9fecf-130">Ne.</span><span class="sxs-lookup"><span data-stu-id="9fecf-130">No.</span></span> <span data-ttu-id="9fecf-131">Uživatelé mohou pokračovat v práci v systému během resetování datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fecf-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="9fecf-132">Uživatelé však nebudou mít přístup k žádným sestavám, které byly vytvořeny pomocí nástroje Financial Reporter, dokud nedojde k dokončení resetu.</span><span class="sxs-lookup"><span data-stu-id="9fecf-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
