---
title: Přehled stránek košíku a pokladny
description: Toto téma poskytuje přehled stránek košíku a pokladny v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e932be31a301ef5aacb68fa4e710d8a9137b7263
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410889"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="685d8-103">Přehled stránek košíku a pokladny</span><span class="sxs-lookup"><span data-stu-id="685d8-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="685d8-104">Toto téma poskytuje přehled stránek košíku a pokladny v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="685d8-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="685d8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="685d8-105">Overview</span></span>

<span data-ttu-id="685d8-106">Stránka košík na webu e-Commerce zobrazuje všechny položky, které odběratel přidal do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="685d8-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="685d8-107">Stránka vozíku je sestavena pomocí modulu košík.</span><span class="sxs-lookup"><span data-stu-id="685d8-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="685d8-108">Modul košíku je kontejner, který hostuje všech modulů, které jsou nutné k prezentaci položek v nákupním košíku.</span><span class="sxs-lookup"><span data-stu-id="685d8-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="685d8-109">Modul vozík může rovněž použít jiné moduly, které zobrazují souhrn objednávek a všechny kódy speciální nabídky, které byly použity pro objednávku odběratele.</span><span class="sxs-lookup"><span data-stu-id="685d8-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="685d8-110">Stránka rezervace na webu e-Commerce představuje krok za krokem, podle kterého se zákazníci budou řídit zadáním všech informací, které jsou požadovány pro uvedení objednávky.</span><span class="sxs-lookup"><span data-stu-id="685d8-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="685d8-111">Modul poklady může obsahovat moduly, které zpracovávají dodací adresu, způsob dopravy, fakturační informace, souhrn objednávky a další informace, které souvisejí s objednávkami zákazníka.</span><span class="sxs-lookup"><span data-stu-id="685d8-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="685d8-112">Stránka košíku</span><span class="sxs-lookup"><span data-stu-id="685d8-112">Cart page</span></span>

<span data-ttu-id="685d8-113">Stránka košíku slouží jako nákupní sáček a zahrnuje všechny položky, které byly přidány do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="685d8-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="685d8-114">Následující ilustrace znázorňuje příklad stránky košíku, která byla sestavena pomocí knihovny modulů a tématu "Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="685d8-114">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Příklad stránky košíku](./media/cart2.PNG)

<span data-ttu-id="685d8-116">HLavní část stránky košíku zobrazuje všechny položky, které odběratel přidal do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="685d8-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="685d8-117">Přednastaveny všechny použitelné slevy.</span><span class="sxs-lookup"><span data-stu-id="685d8-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="685d8-118">Tyto slevy zahrnují složité slevy.</span><span class="sxs-lookup"><span data-stu-id="685d8-118">These discounts include complex discounts.</span></span> <span data-ttu-id="685d8-119">Příklady zahrnují "nákup 3 položky a získej 10% slevu" nebo "kup láhev a batoh a získej slevu 10%."</span><span class="sxs-lookup"><span data-stu-id="685d8-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="685d8-120">V modulu souhrn objednávek je zobrazena částka, která je splatná po použití slev, expedice, daní atd.</span><span class="sxs-lookup"><span data-stu-id="685d8-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="685d8-121">Existuje také modul propagačního kódu, který umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="685d8-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="685d8-122">Odběratel může nakupovat anonymně nebo jako přihlášený uživatel.</span><span class="sxs-lookup"><span data-stu-id="685d8-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="685d8-123">Pokud je odběratel přihlášen, položky v nákupním košíku zůstanou mezi relacemi zachovány.</span><span class="sxs-lookup"><span data-stu-id="685d8-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="685d8-124">Tímto způsobem může zákazník pokračovat v nakupování z více zařízení.</span><span class="sxs-lookup"><span data-stu-id="685d8-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="685d8-125">Z nákupního košíku může odběratel přejít k pokladně.</span><span class="sxs-lookup"><span data-stu-id="685d8-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="685d8-126">Zákazník může zahájit rezervaci jako uživatel typu Host nebo jako přihlášený uživatel.</span><span class="sxs-lookup"><span data-stu-id="685d8-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="685d8-127">Informace o tom, jak vytvořit stránku nákupního košíku, naleznete v tématu [Přidání modulu košíku na stránku](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="685d8-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="685d8-128">Stránka pokladny</span><span class="sxs-lookup"><span data-stu-id="685d8-128">Checkout page</span></span>

<span data-ttu-id="685d8-129">Na stránce pokladny jsou umístěny informace vyžadované k zadání objednávky.</span><span class="sxs-lookup"><span data-stu-id="685d8-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="685d8-130">Následující ilustrace znázorňuje příklad stránky pokladny, která byla sestavena pomocí knihovny modulů.</span><span class="sxs-lookup"><span data-stu-id="685d8-130">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Příklad stránky pokladny](./media/Checkout.PNG)

<span data-ttu-id="685d8-132">Hlavní část stránky pokladny, v níž jsou shromážděny všechny informace o objednávce.</span><span class="sxs-lookup"><span data-stu-id="685d8-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="685d8-133">Tyto informace zahrnují dodací adresu, možnosti dodání a informace o platbě.</span><span class="sxs-lookup"><span data-stu-id="685d8-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="685d8-134">Pokladna má tok krok za krokem, protože informace musí být zadány v určitém pořadí, které má být zpracováno.</span><span class="sxs-lookup"><span data-stu-id="685d8-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="685d8-135">Před vypočítáním nákladů na dodání je například nutné zadat dodací adresu a autorizovat platbu.</span><span class="sxs-lookup"><span data-stu-id="685d8-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="685d8-136">Dodací adresa</span><span class="sxs-lookup"><span data-stu-id="685d8-136">Shipping address</span></span>

<span data-ttu-id="685d8-137">Pokud musí být zboží expedováno, je požadováno dodání adresy.</span><span class="sxs-lookup"><span data-stu-id="685d8-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="685d8-138">Formát adres pro dodání jednotlivých národních prostředí lze konfigurovat v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="685d8-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="685d8-139">Pokud budou například položky expedovány do Spojených států, musí doručovací adresa obsahovat ulici, stát a PSČ.</span><span class="sxs-lookup"><span data-stu-id="685d8-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="685d8-140">Některé základní ověření vstupu se provádí pro pole adresy expedice, jako je například ověření alfanumerických znaků, maximální délka a počet.</span><span class="sxs-lookup"><span data-stu-id="685d8-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="685d8-141">Ačkoli platnost samotné adresy není ověřena, toto ověření lze provést pomocí přizpůsobených služeb třetích stran.</span><span class="sxs-lookup"><span data-stu-id="685d8-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="685d8-142">Dodací adresa je použita pro všechny položky v vozíku, pro který je vybrána možnost "expedice".</span><span class="sxs-lookup"><span data-stu-id="685d8-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="685d8-143">Pokud používáte tok rezervace, který je poskytován v knihovně modulů, jednotlivé položky nákupního košíku nelze odeslat na jiné adresy.</span><span class="sxs-lookup"><span data-stu-id="685d8-143">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="685d8-144">Pokud tuto funkci požadujete, lze ji implementovat pomocí vlastního nastavení modulů rezervace.</span><span class="sxs-lookup"><span data-stu-id="685d8-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="685d8-145">Po dodání adresy expedice jsou zobrazeny metody expedice, které jsou k dispozici v online obchodu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="685d8-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="685d8-146">Způsoby expedice a adresy, které podporují, lze konfigurovat v aplikaci Commerce.</span><span class="sxs-lookup"><span data-stu-id="685d8-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="685d8-147">Platba</span><span class="sxs-lookup"><span data-stu-id="685d8-147">Payment</span></span>

<span data-ttu-id="685d8-148">Dalším krokem v toku pokladny je platba.</span><span class="sxs-lookup"><span data-stu-id="685d8-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="685d8-149">V e-Commerce lze k umísťování objednávek, jako jsou kreditní karty, dárkové poukazy a věrnostní body, použít více způsobů platby.</span><span class="sxs-lookup"><span data-stu-id="685d8-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="685d8-150">Lze také použít kombinaci těchto způsobů platby.</span><span class="sxs-lookup"><span data-stu-id="685d8-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="685d8-151">V závislosti na použitých metodách plateb mohou být vyžadovány další informace.</span><span class="sxs-lookup"><span data-stu-id="685d8-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="685d8-152">Například platba kreditní kartou vyžaduje fakturační adresu.</span><span class="sxs-lookup"><span data-stu-id="685d8-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="685d8-153">Platby kreditních karet jsou zpracovávány pomocí konektoru platby Adyen.</span><span class="sxs-lookup"><span data-stu-id="685d8-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="685d8-154">Věrnostní body</span><span class="sxs-lookup"><span data-stu-id="685d8-154">Loyalty points</span></span>

<span data-ttu-id="685d8-155">Během toku pokladny může odběratel, který je členem věrnostního programu a který má časově rozlišené věrnostní body, vyplatit tyto věrnostní body pro objednávku.</span><span class="sxs-lookup"><span data-stu-id="685d8-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="685d8-156">Modul věrnostní body se zobrazí pouze v případě, že odběratel má existující věrnostní členství.</span><span class="sxs-lookup"><span data-stu-id="685d8-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="685d8-157">Pro uživatele, kteří nejsou členy a uživatelé typu Host, je tento modul skrytý.</span><span class="sxs-lookup"><span data-stu-id="685d8-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="685d8-158">Dárkové poukazy</span><span class="sxs-lookup"><span data-stu-id="685d8-158">Gift cards</span></span>

<span data-ttu-id="685d8-159">Knihovna modulů umožňuje, aby byly pro objednávku uplatněny interní dárkové poukazy.</span><span class="sxs-lookup"><span data-stu-id="685d8-159">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="685d8-160">Chcete-li použít interní dárkový poukaz, je nutné, aby byl zákazník přihlášen.</span><span class="sxs-lookup"><span data-stu-id="685d8-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="685d8-161">Pro zvýšení zabezpečení doporučujeme tok přizpůsobit pomocí osobního identifikačního čísla (PIN) pro interní dárkové poukazy.</span><span class="sxs-lookup"><span data-stu-id="685d8-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="685d8-162">Přihlášení a uživatelé typu Host</span><span class="sxs-lookup"><span data-stu-id="685d8-162">Signed-in and guest users</span></span>

<span data-ttu-id="685d8-163">Zákazník může dokončit proces pokladny jako uživatel typu Host nebo jako přihlášený uživatel.</span><span class="sxs-lookup"><span data-stu-id="685d8-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="685d8-164">Pokud se zákazník přihlásí v aplikaci, budou automaticky načteny informace o účtech, jako jsou například uložené přepravné adresy a uložené podrobnosti platební karty.</span><span class="sxs-lookup"><span data-stu-id="685d8-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="685d8-165">Souhrn objednávky</span><span class="sxs-lookup"><span data-stu-id="685d8-165">Order summary</span></span>

<span data-ttu-id="685d8-166">Položka rezervace zobrazí souhrn položek řádku v vozíku, takže zákazník může ověřit objednávku dříve, než ji zadá.</span><span class="sxs-lookup"><span data-stu-id="685d8-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="685d8-167">Položky řádku nelze upravit v průběhu postupu pokladny.</span><span class="sxs-lookup"><span data-stu-id="685d8-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="685d8-168">Odkaz na košík je však uveden v případě, že uživatel chce přejít zpět a upravit položky řádku.</span><span class="sxs-lookup"><span data-stu-id="685d8-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="685d8-169">Poté, co odběratel poskytne informace o dodávce a fakturaci, zobrazí souhrn objednávky částku, která je splatná po uplatnění věrnostních bodů, dárkových poukazů a dalších plateb.</span><span class="sxs-lookup"><span data-stu-id="685d8-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="685d8-170">E-mail a potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="685d8-170">Order confirmation and email</span></span>

<span data-ttu-id="685d8-171">Když odběratel zadá objednávku, je zadáno číslo potvrzení.</span><span class="sxs-lookup"><span data-stu-id="685d8-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="685d8-172">V tomto okamžiku byla platba autorizována, ale nebyla zaúčtovaná.</span><span class="sxs-lookup"><span data-stu-id="685d8-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="685d8-173">Platba bude účtována pouze v případě, že je objednávka splněna (tj. byla expedována nebo vyzvednuta).</span><span class="sxs-lookup"><span data-stu-id="685d8-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="685d8-174">Po vytvoření objednávky je odběrateli odeslán e-mail s potvrzením objednávky.</span><span class="sxs-lookup"><span data-stu-id="685d8-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="685d8-175">Další informace o tom, jak vytvořit stránku pokladny, naleznete v tématu [Přidání modulu pokladny na stránku](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="685d8-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="685d8-176">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="685d8-176">Additional resources</span></span>

[<span data-ttu-id="685d8-177">Přehled domovské stránky</span><span class="sxs-lookup"><span data-stu-id="685d8-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="685d8-178">Přehled stránek s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="685d8-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="685d8-179">Přehled stránek správy účtů</span><span class="sxs-lookup"><span data-stu-id="685d8-179">Account management pages overview</span></span>](quick-tour-account-management.md)
