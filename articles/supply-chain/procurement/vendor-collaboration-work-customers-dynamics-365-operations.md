---
title: Dodavatelská spolupráce se zákazníky
description: Toto téma popisuje, jak můžete využít spolupráci s dodavatelem k práci s nákupními objednávkami ke sledování zásob na skladě.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 540f4f4e4a047b5bc33c9be387c8940175f5f919
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018141"
---
# <a name="vendor-collaboration-with-customers"></a>Dodavatelská spolupráce se zákazníky

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak můžete využít spolupráci s dodavatelem k práci se zákazníky v aplikaci Microsoft Dynamics 365 Supply Chain Management. Dodavatelé mohou dokončit řadu obchodních procesů z následujících pracovních prostorů:

- **Potvrzení nákupní objednávky** – sledování nákupních objednávek a odpovídání na ně.
- **Nabídky dodavatele** – zobrazení požadavků na nabídku a odpovídání na ně zadáním nabídky.
- **Informace o dodavateli** – zobrazení a aktualizace hlavních dat dodavatele.
- **Fakturace** – práce s fakturami. Toto téma nepokrývá pracovní prostor **Fakturace**. Další informace o tomto pracovním prostoru naleznete v části [Pracovní prostor fakturace dodavatelské spolupráce](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

Dodavatele mohou také monitorovat informace o zásobách dodávky.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Práce s nákupními objednávkami v pracovním prostoru Potvrzení nákupní objednávky

Pracovní prostor **Potvrzení nákupní objednávky** umožňuje reagovat na nákupní objednávky, která vám byly odeslány ke kontrole. Umožňuje také zobrazit informace o nákupních objednávkách, které čekají na akci od odběratele, a objednávkách, které byly potvrzeny, ale jsou stále otevřené.

V pracovním prostoru **Potvrzení nákupní objednávky** existují tři seznamy:

- **Nákupní objednávky ke kontrole** – tento seznam uvádí nákupní objednávky, které vám byly zaslány a čekají na vaši odezvu. Až odpovíte, nákupní objednávka bude ze seznamu odebrána. Pokud odběratel odešle novou verzi nákupní objednávky dříve, než odpovíte na předchozí verzi, zobrazí se pouze nejnovější verze.
- **Čeká se na akci odběratele** - tento seznam zobrazuje nákupní objednávky, na které jste odpověděli, ale zákazník je dosud nepotvrdil. Pokud přijmete nákupní objednávku, můžete ji sledovat v tomto seznamu, dokud se stav nezmění na **Potvrzeno**. Pokud nákupní objednávku odmítnete nebo přijměte se změnami, můžete ji sledovat, dokud zákazník neodešle novou verzi.
- **Otevřené potvrzené nákupní objednávky** - tento seznam zobrazuje všechny nákupní objednávky vašeho účtu, který má stav **Potvrzeno**. Když jsou proti NO plně přijaty produkty nebo služby, NO zmizí ze seznamu.

Pro práci s nákupními objednávkami můžete použít následující stránky:

- **Nákupní objednávky ke kontrole** – Tato stránka obsahuje stejné informace jako seznam v pracovním prostoru **Nákupní objednávky ke kontrole**. Viz dřívější popis v tomto tématu.
- **Historie potvrzení nákupních objednávek dodavatele** – Tato stránka obsahuje všechny nákupní objednávky a všechny verze nákupních objednávek, které byly odeslány dodavateli. Také obsahuje všechny odpovědi, které byly vráceny od dodavatele.
- **Otevřené potvrzené nákupní objednávky** – Tato stránka obsahuje stejné informace jako seznam v pracovním prostoru **Otevřené potvrzené nákupní objednávky**. Viz dřívější popis v tomto tématu.
- **Všechny potvrzené nákupní objednávky** – Tato stránka obsahuje všechny nákupní objednávky, které byly potvrzeny. Nákupní objednávky na této stránce zahrnují objednávky, kde byly přijaty produkty nebo služby. Tento seznam slouží ke sledování nákupních objednávek, ke kterým můžete poslat faktury.

### <a name="responding-to-pos"></a>Odpověď na nákupní objednávky

Nákupní objednávky, které vám odběratel poslal ke kontrole, se zobrazují v pracovním prostoru **Potvrzení nákupní objednávky** a na stránce **Nákupní objednávky ke kontrole**. Po otevření objednávky ji můžete přijmout, odmítnout nebo přijmout se změnami. V záhlaví nákupní objednávky nebo na jednotlivých řádcích mohou být přílohy. Je také možné do odpovědi připojit informace na jednotlivých řádcích nebo v záhlaví nákupní objednávky. Například můžete navrhnout náhradní položku pro jeden z řádků.

Nákupní objednávky můžete zobrazit jako náhled a vytisknout jako soubor PDF pomocí možnosti **Náhled/Tisk**. Můžete také použít akci **Zobrazit dimenze** pro skrytí nebo zobrazení následujících sloupců dimenzí: **Pracoviště** , **Sklad** , **Barva** , **Velikost** , **Styl** a **Konfigurace**. 

Pokud vyberete možnost **Přijmout se změnami** , můžete přijmout nebo odmítnout jednotlivé řádky. U řádků můžete provádět také tyto změny:

- Změna dat nebo množství. Pokud chcete aktualizovat potvrzené datum dodání na všech řádcích, použijte možnost **Aktualizovat data dodání** v záhlaví nákupní objednávky.
- Rozdělení řádků pro jiná data dodání nebo množství.
- Náhrada zboží. Zadejte popis položky a číslo položky do pole **Externí** v části **Podrobnosti řádku**.

Nelze změnit informace o cenách nebo náklady, ale můžete použít poznámky k navržení těchto změn.

Pokud vám zákazník pošle novou verzi nákupní objednávky, bude mít objednávka příponu, která značí, že se jedná o upravenou verzi nákupní objednávky, která byla dříve odeslána. Stránka **Historie potvrzení nákupních objednávek dodavatele** slouží ke sledování historie každé objednávky.

## <a name="monitoring-consignment-inventory"></a>Monitorování zásob dodávky na skladě

Pokud používáte zásoby dodávek, můžete zobrazit rozhraní spolupráce dodavatele k zobrazení informací na následujících stránkách:

- **Nákupní objednávky spotřebovávající zásoby dodávek** – nákupní objednávky pro zásoby dodávek se generují, když odběratel převezme vlastnictví zásob. Tyto nákupní objednávky dodávek jsou zobrazeny pouze na této stránce. Nejsou zahrnuty na stránce **Všechny potvrzené nákupní objednávky**.
- **Přijaté produkty ze zásob dodávky** - Tato stránka uvádí seznam všech transakcí, kde bylo vlastnictví produktů převedeno do společnosti, která spotřebovává zásoby. Tyto informace lze použít k fakturaci zákazníkovi.
- **Zásoby dodávky na skladě** - tato stránka zobrazuje uvedený zásoby dodávky na skladě vlastněné vaší společností, které jsou ale k dispozici ve skladu odběratele.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Práce s požadavky na nabídku v pracovním prostoru Nabídky dodavatele

Pracovní prostor **Nabídky dodavatele** umožňuje zobrazení požadavků na nabídku, k jejichž odpovědi byla vaše společnost přizvána. Je možné také odpovědět na požadavky na nabídku. 

Pracovní prostor rovněž zobrazuje všechny požadavky na nabídku, které jste nezískali, nebo naopak získali. Kromě toho, pokud je systém nakonfigurován pro veřejný sektoru, pracovní prostor zobrazuje veřejně dostupné požadavky na nabídku.

### <a name="viewing-rfqs"></a>Zobrazení požadavků na nabídku

Otevřete pracovní prostor **Nabídky dodavatele** pro přístup k následujícím informacím:

- Vyberte **Pozvánky k nové nabídce** pro zobrazení požadavků na nabídku, ke kterým byla vaše společnost přizvána s odpovědí. Zde lze zobrazit požadavky na nabídku a spustit proces nabídky. Zobrazí se také změněné požadavky na nabídku, na které je třeba odeslat novou nabídku.
- Vyberte **Vrácené nabídky** pro zobrazení požadavků na nabídku, které vám odběratel vrátil, abyste poskytli více informací nebo aktualizovali nabídku.
- Vyberte **Probíhající nabídky** pro zobrazení požadavků na nabídku, na kterých pracujete vy nebo kontaktní osoba zastupující společnost, ale která ještě nebyla odeslána.
- Vyberte **Přidělené nabídky** , když chcete zobrazit, zda vám odběratel přidělil alespoň jednu položku řádku ve vaší nabídce.
- Vyberte **Ztracené nabídky** pro zobrazení nabídek, kde všechny řádky byly odmítnuty.
- Vyberte odkaz **Požadavky na nabídky** pro zobrazení seznamu všech pozvánek požadavků na nabídku dodavatelů a všech nabídek, které byly odeslány. Stránka **Požadavky na nabídky** uvádí seznam všech požadavků na nabídku, kterých se dodavatel účastnil. Můžete hledat podle stavu.
- Vyberte odkaz **Odmítnuté nabídky** pro zobrazení seznamu všech požadavků na nabídku, kde kontaktní osoba dodavatele odmítla nabídku.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Práce s požadavky na nabídku, které jsou veřejně dostupné

Osoby pracující ve veřejném sektoru mohou zobrazit otevřené a vypršené požadavky na nabídku, které byly zpřístupněné veřejně.

- Zvolte odkaz **Otevřené publikované požadavky na nabídky** pro zobrazení seznamu otevřených požadavků na nabídku, které jsou k dispozici veřejně. Otevřený požadavek na nabídku je požadavek, který ještě nevypršel. Čas a datum vypršení platnosti naleznete v záhlaví požadavku na nabídku.

    Pokud jste byli přizváni k nabídce, můžete vyhledat stejný požadavek na nabídku na stránce **Pozvánky k nové nabídce**. V některých případech může být zapotřebí vytvořit nabídku k otevřenému požadavku na nabídku, ke kterému jste nebyli přizváni. V takovém případě se můžete přizvat sami, za předpokladu, že odběratel povolil možnost přizvat se sám k případu požadavku na nabídku.

- Zvolte odkaz **Uzavřené publikované požadavky na nabídky** pro zobrazení seznamu uzavřených požadavků na nabídku, které jsou k dispozici veřejně. Uzavřený požadavek na nabídku je požadavek, který vypršel. Čas a datum vypršení platnosti naleznete v záhlaví požadavku na nabídku.

    Uzavřený požadavek na nabídku zobrazuje všechny nabídky dodavatele až na úroveň řádku. Jak jsou nabídky přidělovány nebo odmítány, promítá se tato informace do uzavřeného požadavku na nabídku. Jakékoli přílohy, které jsou zahrnuty do nabídky, jsou rovněž k dispozici.

**Poznámka:** Tato funkce je k dispozici pouze v případě, že je povolena konfigurace veřejného sektoru.

### <a name="bidding"></a>Nabídky

- Klikněte na tlačítko **Nabídka** a spusťte nabídky na požadavek na nabídku.

    Pokud jsou povoleny úpravy pro pole nabídky na záhlavích a řádcích požadavku na nabídku, můžete zadávat nabídku přímo do mřížky řádků. Rovněž je třeba zvážit všechny další informace o nabídce, které mají být přidány do podrobností řádku.

    Při zahájení práce na nabídce se tato skutečnost zobrazí v části **Probíhající nabídky**.

    Nabídku lze uložit kdykoli před datem vypršení platnosti. Poté se lze vrátit později a dokončit a odeslat nabídku. Po odeslání nabídky ji lze opět vyvolat a aktualizovat, dokud nevyprší platnost.

- Vyberte **Resetovat z požadavku na nabídku** k resetování dat zadaných pro nabídku a návratu k původnímu požadavku na nabídku. Můžete resetovat záhlaví nebo řádek.
- Vyberte **Přidat alternativu** nebo **Odebrat alternativu** v mřížce řádku, abyste mohli pracovat s alternativami.

    Některé požadavky na nabídku umožňují alternativní nabídky. Můžete zadat alternativní nabídky pouze pro řádky typu **Kategorie** , protože určité položky nelze přidat jako alternativy. 

- Vyberte **Příloha požadavku na nabídku** nebo **Příloha řádků požadavku na nabídku** a otevřete jakoukoliv přílohu, kterou odběratel přidal do požadavku na nabídku. Vyberte **Přílohy nabídky** nebo **Přílohy řádku nabídky** k odeslání příloh spolu s nabídkou.

    Mohou existovat dotazníky, na které musí odpovědět předtím, než můžete odeslat nabídku.

- Vyberte **Odmítnout** , pokud se nechcete nabídky účastnit. Po zvolení možnosti **Odmítnout** nelze opětovně vyvolat akci a zadat nabídku.

Pokud je požadavek na nabídku změněn, je nutné zadat novou nabídku. Informace o změně naleznete na kartě **Dodatky** na stránce požadavku na nabídku. Změněné požadavky na nabídku se zobrazí na stránce **Pozvánky k nové nabídce**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Přístup k hlavním datům dodavatele v pracovním prostoru Informace o dodavateli

Jako dodavatel můžete přistupovat k části informací, které odběratel spravuje v hlavním záznamu o dodavateli. Z toho vyplývá, že můžete udržovat informace aktuální. Chcete-li aktualizovat informace, musíte mít roli správce dodavatele (externí).

Dostupné informace jsou název dodavatele, adresy, kontaktní informace, kontaktní osoby a jejich kontaktní informace, identifikační čísla, registrační čísla daně, kategorie zásobování, pro které je dodavatel schválen při prodeji odběrateli, a informace o certifikátech.

## <a name="additional-resources"></a>Další zdroje

[Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md)
