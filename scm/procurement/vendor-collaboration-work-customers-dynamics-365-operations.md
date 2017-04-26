---
title: "Spolupráce dodavatelů s odběrateli"
description: "Toto téma popisuje, jak můžete využít spolupráci s dodavatelem k práci s nákupními objednávkami v aplikaci Microsoft Dynamics 365 for Operations ke sledování zásob na skladě."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Spolupráce dodavatelů s odběrateli

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak můžete využít spolupráci s dodavatelem k práci s nákupními objednávkami v aplikaci Microsoft Dynamics 365 for Operations ke sledování zásob na skladě.

Toto téma popisuje, jak můžete využít spolupráci s dodavatelem k práci se zákazníky v aplikaci Microsoft Dynamics 365 for Operations. Obsahuje informace o sledování a odpovídání na nákupní objednávky a sledování šarže zásob. Je také možné použít pro práci s fakturami spolupráce dodavatele. Další informace naleznete v tématu [fakturace pracovní prostor spolupráce dodavatele](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Práce s nákupními objednávkami
Pracovní prostor **Potvrzení nákupní objednávky** umožňuje reagovat na nákupní objednávku, která vám byl odeslána ke kontrole. Umožňuje také zobrazit informace o nákupních objednávkách, které čekají na akci od odběratele a objednávkách, které byly potvrzeny, ale jsou stále otevřené. V pracovním prostoru **Potvrzení nákupní objednávky** existují tři seznamy:

-   **Nákupní objednávky pro přezkoumání** -tento seznam zobrazuje POs, která vám byla odeslána a čeká na odpověď od vás. Po reakci, No zmizí ze seznamu. Pokud odběratel odešle novou verzi nákupní objednávky dříve než odpovíte na předchozí, zobrazí se pouze nejnovější verze.
-   **Čeká se na akce odběratele** - tento seznam vám umožní zobrazit PO, na které jste odpověděli, avšak nebyly dosud potvrzeny odběratelem. Pokud jste přijali nákupní objednávky, můžete je sledovat v tomto seznamu, dokud se stav nezmění na **Potvrzeno**. Pokud nákupní objednávku odmítnete nebo přijměte se změnami, můžete sledovat nákupní objednávku v tomto poli, dokud zákazník neodešle novou verzi.
-   **Otevřené potvrzené nákupní objednávky** - tento seznam obsahuje všechny nákupní objednávky účtu, který má stav **Potvrzeno**. Když jsou proti NO plně přijaty produkty nebo služby, NO zmizí ze seznamu.

Následující seznam obsahuje čtyři stránky, které lze použít pro práci s nákupní objednávkami. Dvě z nich obsahují stejné informace, jako jsou seznamy v pracovním prostoru:

-   **Nákupní objednávky ke kontrole** (viz výše)
-   **Historie potvrzení nákupních objednávek dodavatele** - Tato stránka obsahuje všechny Nákupní objednávky a všechny verze nákupních objednávek, které byly odeslány dodavateli, a všechny odpovědi, které byly vráceny od dodavatele.
-   **Otevření potvrzených nákupních objednávek** (viz výše)
-   **Všechny potvrzené nákupní objednávky** - Tato stránka obsahuje všechny potvrzené nákupní objednávky, včetně těch, pro které byly přijaty produkty nebo služby. Tento seznam slouží ke sledování, ke kterým nákupním objednávkám můžete posílat faktury.

### <a name="responding-to-purchase-orders"></a>Reagování na nákupní objednávky

Jsou viditelné v nákupních objednávek, které zákazník poslal ke kontrole **potvrzení nákupní objednávky** prostoru a na **nákupní objednávky pro přezkoumání** stránky. Po otevření objednávky, můžete ji přijmout, odmítnout nebo přijmout změny. V záhlaví nákupní objednávky nebo na jednotlivých řádcích mohou být přílohy. Je také možné do odpovědi připojit informace na jednotlivých řádcích nebo v záhlaví nákupní objednávky. Například můžete navrhnout náhradní položku pro jeden z řádků. Nákupní objednávky můžete zobrazit jako náhled a vytisknout jako soubor PDF pomocí možnosti **Náhled/Tisk**. Následující sloupce dimenzí můžete zobrazit nebo skrýt pomocí akce **Zobrazit dimenze**: Středisko, Sklad, Barva, Velikost, Styl, Konfigurace. Použijete-li **přijmout změny** možnost, můžete přijmout nebo odmítnout jednotlivé řádky. Řádky můžete provést také následující změny:

-   Změna dat nebo množství. Pokud chcete aktualizovat potvrzené datum dodání na všech řádcích, použijte možnost **Aktualizovat data dodání** v záhlaví nákupní objednávky.
-   Rozdělení řádků pro jiná data dodání nebo množství
-   Náhrada zboží. Abyste to mohli provést, zadejte popis položky a číslo položky do pole **Externí** v části **Podrobnosti řádku**.

Nelze změnit informace o cenách nebo náklady, ale můžete navrhovat jejich změny pomocí poznámek. Pokud vám zákazník pošle novou verzi nákupní objednávky, bude mít objednávka příponu, která značí, že se jedná o upravenou verzi nákupní objednávky té, která byla dříve předána. Stránka **Historie potvrzení nákupních objednávek dodavatele** slouží ke sledování historie každé objednávky.

## <a name="monitoring-consignment-inventory"></a>Monitorování zásob dodávky na skladě
Pokud používáte zásoby na skladě, můžete zobrazit rozhraní spolupráce dodavatele k zobrazení informací na následujících stránkách:

-   **Nákupní objednávky využívající dodávku zásob** -nákupní objednávky pro dodávku zásob jsou generovány, když zákazník převezme vlastnictví zásob. Tyto nákupní objednávky se zobrazí pouze na stránce **Nákupní objednávky spotřebovávající zásoby dodávek**. Nejsou zahrnuty na stránce **Všechny potvrzené nákupní objednávky**.
-   **Přijaté produkty ze zásob dodávky** - Tato stránka uvádí seznam všech transakcí, kde bylo vlastnictví produktů převedeno do společnosti, která využívá zásoby. Tyto informace lze použít k fakturaci zákazníkovi.
-   **Zásoby dodávky na skladě** - tato stránka zobrazuje uvedený zásoby zásilky na skladě vlastněné vaší společností, které jsou k dispozici ve skladu odběratele.


<a name="see-also"></a>Viz také
--------

[Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md)




