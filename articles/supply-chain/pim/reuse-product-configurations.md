---
title: Opětovně použít konfigurace produktu
description: Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu. Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele. Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21dc25b878ff65b57b060fe3d74b5d120fa4b5cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260592"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="08eb0-105">Opětovně použít konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="08eb0-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08eb0-106">Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu.</span><span class="sxs-lookup"><span data-stu-id="08eb0-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="08eb0-107">Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele.</span><span class="sxs-lookup"><span data-stu-id="08eb0-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="08eb0-108">Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup.</span><span class="sxs-lookup"><span data-stu-id="08eb0-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="08eb0-109">Požadavky na opětovné použití konfigurací</span><span class="sxs-lookup"><span data-stu-id="08eb0-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="08eb0-110">Pokud chcete povolit opětovné použití konfigurací, je nutné zadat pro komponenty a atributy na stránce **Podrobnosti modelu konfigurace produktu** následující informace:</span><span class="sxs-lookup"><span data-stu-id="08eb0-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="08eb0-111">**Komponenty a dílčí komponenty** – Na pevné záložce **Obecné** v poli **Znovu použít konfigurace** vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="08eb0-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="08eb0-112">**Atributy** – na pevné záložce **Atributy** vyberte možnost **Zahrnout do opakovaného použití**.</span><span class="sxs-lookup"><span data-stu-id="08eb0-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="08eb0-113">Tato možnost se zobrazí, pouze pokud je související komponenta povolena pro opakované použití.</span><span class="sxs-lookup"><span data-stu-id="08eb0-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="08eb0-114">Jestliže nevyberete žádné atributy pro opakované použití, konfigurace je vždy znovu použita bez ohledu na to, co uživatel vybere během konfigurační relace.</span><span class="sxs-lookup"><span data-stu-id="08eb0-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="08eb0-115">Hodnoty atributů v existující konfiguraci musí odpovídat výběrům uživatele.</span><span class="sxs-lookup"><span data-stu-id="08eb0-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="08eb0-116">Když například uživatel vybere jako barvu během relace konfigurace **Modrá**, systém ověří, zda existující konfigurace obsahuje komponenty modrou barvu.</span><span class="sxs-lookup"><span data-stu-id="08eb0-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="08eb0-117">Resetování opětovného použití konfigurace</span><span class="sxs-lookup"><span data-stu-id="08eb0-117">Resetting configuration reuse</span></span>
<span data-ttu-id="08eb0-118">Při resetování opětovného použití konfigurací se přestanou brát v úvahu dříve vytvořené konfigurace.</span><span class="sxs-lookup"><span data-stu-id="08eb0-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="08eb0-119">Můžete resetovat opětovné použití konfigurací, pokud byl změněn kusovník nebo postup, ale nebyly změněny žádné související atributy.</span><span class="sxs-lookup"><span data-stu-id="08eb0-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="08eb0-120">Opětovné použití konfigurací se resetuje na pevné záložce **Obecné** komponenty.</span><span class="sxs-lookup"><span data-stu-id="08eb0-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]