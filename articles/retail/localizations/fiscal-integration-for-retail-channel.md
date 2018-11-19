---
title: "Fiskální integrace pro maloobchodní síť"
description: "V tomto tématu je uveden přehled fiskální integrace pro Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: cs-cz
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="7cf02-103">Fiskální integrace pro maloobchodní síť</span><span class="sxs-lookup"><span data-stu-id="7cf02-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cf02-104">Toto téma poskytuje přehled o funkci fiskální integrace, která je k dispozici v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="7cf02-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="7cf02-105">Funkci fiskální integrace je architektura navržená pro podporu místních daňových předpisů, které mají za cíl zabránit podvodům v oblasti maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="7cf02-106">Typický scénáře, které lze pokrýt pomocí fiskální integrace, zahrnují:</span><span class="sxs-lookup"><span data-stu-id="7cf02-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="7cf02-107">Tisk fiskální příjemky a její předání odběrateli.</span><span class="sxs-lookup"><span data-stu-id="7cf02-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="7cf02-108">Zabezpečení odeslání informací týkajících se prodeje a vrácení provedených na POS do externí služby poskytované úřadem.</span><span class="sxs-lookup"><span data-stu-id="7cf02-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="7cf02-109">Použití ochrany dat pomocí digitálního podpisu autorizovaného úřadem..</span><span class="sxs-lookup"><span data-stu-id="7cf02-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="7cf02-110">Toto téma obsahuje pokyny pro nastavení fiskální integrace, aby mohli uživatelé provádět následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="7cf02-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="7cf02-111">Konfigurovat fiskální konektory, které jsou fiskálními zařízeními nebo službami používanými pro účely fiskální registrace, jako je ukládání, digitální podpisy a zabezpečené odeslání fiskálních dat.</span><span class="sxs-lookup"><span data-stu-id="7cf02-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="7cf02-112">Konfigurovat poskytovatele dokumentu, který definuje výstupní metodu a algoritmus generování fiskálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="7cf02-113">Konfigurovat proces fiskální registrace, který definuje postupnost kroků a skupinu konektorů použitých v každém kroku.</span><span class="sxs-lookup"><span data-stu-id="7cf02-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="7cf02-114">Přiřadit procesy fiskální registrace do funkčních profilů POS.</span><span class="sxs-lookup"><span data-stu-id="7cf02-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="7cf02-115">Přiřadit technické profily konektorů buď k hardwarovým profilům (pro místní fiskální konektory) nebo k funkčním profilům POS (pro jiné typy fiskálních konektorů).</span><span class="sxs-lookup"><span data-stu-id="7cf02-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="7cf02-116">Tok provádění fiskální integrace</span><span class="sxs-lookup"><span data-stu-id="7cf02-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="7cf02-117">Následující scénář zobrazí běžný tok provádění fiskální integrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="7cf02-118">Inicializace procesu fiskální registrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="7cf02-119">Po provedení některých kroků, kdy je vyžadována fiskální registrace, například po uzavření maloobchodní transakce, je proces fiskální registrace přidružen k aktuálnímu funkčnímu profilu POS.</span><span class="sxs-lookup"><span data-stu-id="7cf02-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="7cf02-120">Vyhledávání fiskálního konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="7cf02-121">Pro každý krok fiskální registrace zahrnutý v procesu fiskální registrace se systém spáruje se seznamem fiskálních konektorů.</span><span class="sxs-lookup"><span data-stu-id="7cf02-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="7cf02-122">Tyto konektory mají funkční profil obsažený ve specifikované skupině konektorů se seznamem konektorů, které mají technický profil přidružený k aktuálnímu hardwarovému profilu (u typu konektoru, který se rovná pouze hodnotě **Místní**) nebo k aktuálnímu funkčnímu profilu POS (pro jiné typy konektorů).</span><span class="sxs-lookup"><span data-stu-id="7cf02-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="7cf02-123">Provedení fiskální integrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="7cf02-124">Systém provede všechny potřebné akce definované sestavením propojeným s nalezeným konektorem.</span><span class="sxs-lookup"><span data-stu-id="7cf02-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="7cf02-125">To se provádí v souladu s nastavením funkčního profilu a technického profilu, které byly pro tento konektor nalezeny v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="7cf02-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="7cf02-126">Nastavení nutné před použitím fiskální integrace</span><span class="sxs-lookup"><span data-stu-id="7cf02-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="7cf02-127">Před použitím funkce fiskální integrace byste měli definovat následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="7cf02-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="7cf02-128">Definujte číselné řady na stránce **Parametry maloobchodu** pro číslo fiskálního funkčního profilu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="7cf02-129">Definujte číselné řady na stránce **Sdílené parametry maloobchodu** pro následující odkazy:</span><span class="sxs-lookup"><span data-stu-id="7cf02-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="7cf02-130">Číslo fiskálního technického profilu</span><span class="sxs-lookup"><span data-stu-id="7cf02-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="7cf02-131">Číslo skupiny fiskálních konektorů</span><span class="sxs-lookup"><span data-stu-id="7cf02-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="7cf02-132">Číslo procesu registrace</span><span class="sxs-lookup"><span data-stu-id="7cf02-132">Registration process number</span></span>

- <span data-ttu-id="7cf02-133">Vytvořte **Fiskální konektor** v nastavení **Maloobchod > Nastavení kanálu> Fiskální integrace > Fiskální konektory** pro každé zařízení nebo službu, které chcete použít pro účely fiskální integrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="7cf02-134">Vytvořte **Poskytovatele fiskálního dokumentu** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Poskytovatelé fiskálních dokumentů** pro všechny fiskální konektory.</span><span class="sxs-lookup"><span data-stu-id="7cf02-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="7cf02-135">Mapování dat je považováno za součást poskytovatele fiskálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="7cf02-136">Chcete-li nastavit různá mapování dat pro stejný konektor (například pravidla pro konkrétní stav), měli byste vytvořit různé poskytovatele fiskálních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="7cf02-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="7cf02-137">Vytvořte **Funkční profil konektoru** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Funkční profily konektoru** pro každého poskytovatele fiskálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="7cf02-138">Zvolte název konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-138">Select a connector name.</span></span>
  - <span data-ttu-id="7cf02-139">Vyberte poskytovatele dokumentu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-139">Select a document provider.</span></span>
  - <span data-ttu-id="7cf02-140">Určete nastavení sazeb DPH na kartě **Nastavení služby**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="7cf02-141">Určete mapování kódů DPH a mapování typu úhrady na kartě **Mapování dat**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="7cf02-142">Příklad</span><span class="sxs-lookup"><span data-stu-id="7cf02-142">Examples</span></span> 

  |  | <span data-ttu-id="7cf02-143">Formát</span><span class="sxs-lookup"><span data-stu-id="7cf02-143">Format</span></span> | <span data-ttu-id="7cf02-144">Příklad</span><span class="sxs-lookup"><span data-stu-id="7cf02-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="7cf02-145">Nastavení sazeb DPH</span><span class="sxs-lookup"><span data-stu-id="7cf02-145">VAT rates settings</span></span> | <span data-ttu-id="7cf02-146">hodnota : VATrate</span><span class="sxs-lookup"><span data-stu-id="7cf02-146">value : VATrate</span></span> | <span data-ttu-id="7cf02-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="7cf02-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="7cf02-148">Mapování kódů DPH</span><span class="sxs-lookup"><span data-stu-id="7cf02-148">VAT codes mapping</span></span> | <span data-ttu-id="7cf02-149">VATcode : hodnota</span><span class="sxs-lookup"><span data-stu-id="7cf02-149">VATcode : value</span></span> | <span data-ttu-id="7cf02-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="7cf02-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="7cf02-151">Mapování typů úhrad</span><span class="sxs-lookup"><span data-stu-id="7cf02-151">Tender types mapping</span></span> | <span data-ttu-id="7cf02-152">TenderTyp : hodnota</span><span class="sxs-lookup"><span data-stu-id="7cf02-152">TenderTyp : value</span></span> | <span data-ttu-id="7cf02-153">Hotovost : 1, Karta : 2</span><span class="sxs-lookup"><span data-stu-id="7cf02-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="7cf02-154">Vytvořte **Skupiny fiskálních konektorů** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Skupina fiskálních konektorů**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="7cf02-155">Skupina konektoru je podmnožinou funkčních profilů propojených s fiskálními konektory, které provádí identické funkce a používají se ve stejné fázi v rámci procesu fiskální registrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="7cf02-156">Přidání funkčních profilů do skupiny konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="7cf02-157">Klikněte na **Přidat** na stránce **Funkční profily** a vyberte číslo profilu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="7cf02-158">Pokud chcete pozastavit použití funkčního profilu, nastavte **Zakázat** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="7cf02-159">Tato změna ovlivní pouze aktuální skupinu konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-159">This change affects the current connector group only.</span></span> <span data-ttu-id="7cf02-160">Můžete pokračovat s použitím stejného funkčního profilu v jiných skupinách konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="7cf02-161">Ve skupině konektoru může mít každý fiskální konektor pouze jeden funkční profil.</span><span class="sxs-lookup"><span data-stu-id="7cf02-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="7cf02-162">Vytvořte **Technický profil konektoru** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Technické profily konektoru** pro každý fiskální konektor.</span><span class="sxs-lookup"><span data-stu-id="7cf02-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="7cf02-163">Zvolte název konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-163">Select a connector name.</span></span>
  - <span data-ttu-id="7cf02-164">Zvolte typ konektoru:</span><span class="sxs-lookup"><span data-stu-id="7cf02-164">Select a connector type:</span></span> 
      - <span data-ttu-id="7cf02-165">**Místní** – Nastavte tento typ pro fyzická zařízení nebo aplikace nainstalované v místním počítači.</span><span class="sxs-lookup"><span data-stu-id="7cf02-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="7cf02-166">**Interní** – Nastavte tento typ pro fiskální zařízení a služby připojené k serveru Retail Server.</span><span class="sxs-lookup"><span data-stu-id="7cf02-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="7cf02-167">**Externí** – Pro externí fiskální služby, jako je webový portál poskytovaný finančním úřadem.</span><span class="sxs-lookup"><span data-stu-id="7cf02-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="7cf02-168">Zadejte nastavení na kartě **Připojení**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="7cf02-169">Aktualizovaná verze konfigurace, která byla načtena dříve, bude načtena pro technické i funkční profily.</span><span class="sxs-lookup"><span data-stu-id="7cf02-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="7cf02-170">Je-li již použit vhodný konektor nebo poskytovatel dokumentů, budete upozorněni.</span><span class="sxs-lookup"><span data-stu-id="7cf02-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="7cf02-171">Ve výchozím nastavení budou všechny změny provedené ručně ve funkčních a technických profilech uloženy.</span><span class="sxs-lookup"><span data-stu-id="7cf02-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="7cf02-172">Chcete-li tyto profily přepsat pomocí výchozí sady parametrů z konfigurace, klikněte na tlačítko **Aktualizovat** na stránce **Funkční profily konektoru** a na stránce **Technické profily konektoru**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="7cf02-173">Vytvořite **Proces fiskální registrace** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Procesy fiskální registrace** pro každý jedinečný proces fiskálních integrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="7cf02-174">Registrační proces je definován sledem registračních kroků a skupinou konektorů používaných v každém kroku.</span><span class="sxs-lookup"><span data-stu-id="7cf02-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="7cf02-175">Přidejte kroky registrace do procesu:</span><span class="sxs-lookup"><span data-stu-id="7cf02-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="7cf02-176">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-176">Click **Add**.</span></span>
      - <span data-ttu-id="7cf02-177">Zvolte typ konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="7cf02-178">Toto pole určuje, kde bude systém hledat konektor v technickém profilu, a to buď v hardwarovém profilu pro konektor typu **Místní**, nebo ve funkčních profilech pro jiné typy fiskálních konektorů.</span><span class="sxs-lookup"><span data-stu-id="7cf02-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="7cf02-179">Zvolte skupinu konektorů.</span><span class="sxs-lookup"><span data-stu-id="7cf02-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="7cf02-180">Klikněte na tlačítko **ověřit** pro kontrolu integrity struktury procesu registrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="7cf02-181">Doporučujeme, aby ověření byla provedena v následujících případech:</span><span class="sxs-lookup"><span data-stu-id="7cf02-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="7cf02-182">Pro nový proces registrace po dokončení všech nastavení, včetně vazby na funkční profily POS a hardwarové profily.</span><span class="sxs-lookup"><span data-stu-id="7cf02-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="7cf02-183">Po provedení aktualizací existujícího procesu registrace.</span><span class="sxs-lookup"><span data-stu-id="7cf02-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="7cf02-184">Navázání procesů fiskální registrace na funkční profily POS v **Maloobchod > Nastavení kanálu > Nastavení POS > Profily POS > Funkční profily**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="7cf02-185">Klikněte na tlačítko **Upravit** a vyberte **Číslo procesu** na kartě **Proces fiskální registrace**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="7cf02-186">Navažte technický profil konektoru na hardwarový profil v **Maloobchod > Nastavení kanálu > Nastavení POS > Profily POS > Hardwarové profily**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="7cf02-187">Klikněte na tlačítko **Upravit** a potom klikněte na tlačítko **Nový** na kartě **Fiskální technický profil**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="7cf02-188">Zvolte technický profil konektoru v poli **Číslo profilu**.</span><span class="sxs-lookup"><span data-stu-id="7cf02-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="7cf02-189">Můžete přidat několik technických profilů k hardwarovému profilu.</span><span class="sxs-lookup"><span data-stu-id="7cf02-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="7cf02-190">To však není podporováno, pokud hardwarový profil má více než jeden průsečík s jakoukoliv skupinou konektoru.</span><span class="sxs-lookup"><span data-stu-id="7cf02-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="7cf02-191">Abyste se vyhnuli nesprávnému nastavení, doporučujeme ověřit proces registrace po aktualizaci všech hardwarových profilů.</span><span class="sxs-lookup"><span data-stu-id="7cf02-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

