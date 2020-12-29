---
title: Rychlý import a export
description: Účel funkce Rychlý import / export je umožnit provádění importu a exportu za použití menšího počtu kroků.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: c5425f53ba66b4123457154386bf51342697fbd1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683195"
---
# <a name="quick-import-export"></a><span data-ttu-id="99cb1-103">Rychlý import a export</span><span class="sxs-lookup"><span data-stu-id="99cb1-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99cb1-104">Účel funkce Rychlý import / export je umožnit provádění importu a exportu za použití menšího počtu kroků.</span><span class="sxs-lookup"><span data-stu-id="99cb1-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="99cb1-105">Funkci Rychlý Import / Export jsme přidali, aby měli uživatelé možnost importovat nebo exportovat jednoduché úlohy, které chtějí provést rychle.</span><span class="sxs-lookup"><span data-stu-id="99cb1-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="99cb1-106">V ideálním případě se tato funkce používá v situacích, ve kterých je soubor namapován automaticky do systému, a uživatel nemusí procházet rozšířeným mapováním nebo vytvářet opakovaně úlohy pro import nebo export.</span><span class="sxs-lookup"><span data-stu-id="99cb1-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="99cb1-107">Tato funkce podporuje práci se standardními i upravenými entitami.</span><span class="sxs-lookup"><span data-stu-id="99cb1-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="99cb1-108">Můžete importovat ze souborů, a pokud používáte zdroj dat ODBC, můžete vybrat dotaz a použít jej k definování importu.</span><span class="sxs-lookup"><span data-stu-id="99cb1-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="99cb1-109">Je třeba mít již definované formáty zdrojových dat pro AX nebo pro soubor, a vědět, kde jsou umístěny.</span><span class="sxs-lookup"><span data-stu-id="99cb1-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="99cb1-110">Funkce Rychlý import / export nevyžaduje vytvoření skupiny pro zpracování – skupina bude automaticky vytvořena systémem při provádění importu nebo exportu.</span><span class="sxs-lookup"><span data-stu-id="99cb1-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="99cb1-111">Můžete také zachovat historii dat importovaných pomocí funkce Rychlý import / export.</span><span class="sxs-lookup"><span data-stu-id="99cb1-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="99cb1-112">Mějte na paměti, že funkce Rychlý import / export předpokládá, že jste obeznámeni s konceptem DIXF.</span><span class="sxs-lookup"><span data-stu-id="99cb1-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>



