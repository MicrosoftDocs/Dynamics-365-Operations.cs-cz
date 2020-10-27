---
title: Poskytování příruček v hybridní realitě pro pracovníky ve výrobě
description: Toto téma vysvětluje, jak modul řízení výroby v Microsoft Dynamics 365 Supply Chain Management integrovat s Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989262"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Poskytování příruček v hybridní realitě pro pracovníky ve výrobě

Pracovníci ve výrobních procesech využijí relevantní pokyny, které jsou jim poskytovány ve správný čas v souvislosti s jejich prací. *Pokyny* se používají v několika oblastech práce, mezi které patří: montáž, servis, provozu, certifikace a bezpečnost. Průběžná instruktáž ve všech těchto základních firemních funkcích pomůže pracovníkům dosáhnout lepších výsledků a lépe pracovat.

## <a name="introduction"></a>Úvod

Pokyny můžete poskytovat různými způsoby. Jeden dodávaný efektivní systém využívá [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides dokáže vaše zaměstnance posílit pomocí praktického učení. Můžete definovat standardizované procesy s podrobnými pokyny, které vaše zaměstnance navedou na potřebné nástroje a součásti a ukážou jim, jak tyto nástroje používat v reálných pracovních situacích.

Příručky můžete připojit k různým aspektům řízení výroby, mezi které patří:

- [Prostředky](#resources)
- [Skupiny prostředků](#resource-groups)
- [Uvolněné produkty](#released-products)
- [Receptury](#formulas)
- [Verze receptury](#formula-versions)
- [Kusovníky](#bom)
- [Verze kusovníků](#bom-versions)
- [Postupy](#routes)
- [Verze postupu](#route-versions)
- [Vztahy operací postupu](#route-operation-relations)

> [!NOTE]
> Příručky můžete rovněž připojit ke správě majetku. Další informace o této možnosti najdete v tématu [Integrace Dynamics 365 Supply Chain Management (Správa majetku) s Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Když si pracovník v první linii vybere prostřednictvím Supply Chain Management v dílně nějaký úkol, uvidí na úkolovém lístku [příslušné příručky](#logic). Když si pracovník vybere konkrétní příručku, ukáže se na obrazovce kód QR příslušné příručky. Pracovník pak pomocí svých HoloLens naskenuje kód QR, který spustí aplikaci Guides a zobrazí požadované pokyny.

V následujících pododdílech je popsáno několik vybraných scénářů, ve kterých mohou firmy z různých odvětví vidět největší hodnotu při použití aplikace Guides k prezentaci pokynů pro výrobu.

### <a name="assembly"></a>Sestavení

![Použití aplikace Guides při montáži](media/instruction-guides-hero-assembly.png "Použití aplikace Guides při servisu")

Pokyny v montážních operacích ukazují pracovníkům potřebné nástroje a součásti a způsob, jakým se používají v reálných pracovních situacích.

Manažeři výroby mohou vytvářet a přiřazovat příručky například pro [výrobní postupy](routes-operations.md), [vztahy mezi operacemi](routes-operations.md#operation-relations) nebo [kusovníky](bill-of-material-bom.md). V dílně najdou pracovníci příslušné pokyny u odpovídající operace.

### <a name="service"></a>Servis

![Použití aplikace Guides při servisu](media/instruction-guides-hero-service.png "Použití aplikace Guides při servisu")

Vybavte techniky pokyny v místě výkonu práce, což eliminuje potřebu plánování dalších návštěv.

Manažeři servisu mohou příručky přiřadit například ke konkrétním [produktům](../../commerce/product.md), které podstupují posouzení kvality.

### <a name="quality"></a>Kvalita

![Použití aplikace Guides při kontrole kvality](media/instruction-guides-hero-quality.png "Použití aplikace Guides při kontrole kvality")

Při zavádění nových procesů můžete přeměnou znalostí zaměstnanců na opakovaně použitelný nástroj zajistit větší konzistenci.

Manažeři kvality mohou příručky přiřadit například ke konkrétním [produktům](../../commerce/product.md), které podstupují posouzení kvality.

### <a name="certifications"></a>Certifikáty

![Použití aplikace Guides při úkolech spojených s certifikací](media/instruction-guides-hero-certification.png "Použití aplikace Guides při úkolech spojených s certifikací")

Rychlou identifikací toho, kdo a kde potřebuje pomoc, můžete zajistit, aby každý zaměstnanec splňoval vysoké standardy.

### <a name="safety"></a>Bezpečnost

![Použití aplikace Guides v pokynech pro bezpečnost práce](media/instruction-guides-hero-safety.png "Použití aplikace Guides v pokynech pro bezpečnost práce")

Připravte pokyny, které procházejí nebezpečné postupy virtuálně předtím, než se realizují ve fyzickém prostředí. Díky hybridní realitě mohou pracovníci nebezpečné postupy zažít virtuálně.

Vedoucí výroby mohou připravit specializované pokyny pro manipulaci s nebezpečným materiálem nebo choulostivé manipulační postupy a přiřadit je k [vyráběným položkám](../../commerce/product.md), [postupům](routes-operations.md) a [operacím](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Začínáme s pokyny a aplikací Guides

Chcete-li povolit pokyny ve výrobních procesech, nabízí Supply Chain Management integraci s Dynamics 365 Guides. K vytváření, údržbě a přiřazování pokynů v hybridní realitě k výrobním prostředkům a práci se vyžaduje licencovaná a nainstalovaná instance aplikace Guides.

### <a name="prerequisites"></a>Předpoklady

Abyste mohli tuto funkci používat, musí váš systém obsahovat:

- Dynamics 365 Supply Chain Management verze 10.0.15 nebo novější
- [Duální zápis](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) pro aplikace Supply Chain Management.
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) verze 400.0.1.48 nebo novější

### <a name="turn-on-the-feature"></a>Zapnutí funkce

Chcete-li tuto funkci ve svém systému zpřístupnit, musíte povolit její konfigurační klíče. Stačí, když to uděláte jen jednou. Jako správce musíte provést následující postup:

1. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence** .
1. Rozbalte oddíl **Hybridní realita** a zaškrtněte políčko **Příručka v hybridní realitě** .
1. Rozbalte oddíl **Řízení výroby** a zaškrtněte políčko **Výrobní pokyny** .
1. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Konfigurace způsobu, jakým se aplikace Guides zobrazuje v dílně

Chcete-li nakonfigurovat, jak se aplikace Guides bude zobrazovat v dílně, přejděte na **Hybridní realita \>Dynamics 365 Guides\> Konfigurovat integraci aplikace Guides** .

![Konfigurace integrace aplikace Guides ve výrobě](media/instruction-guides-configure-integration.png "Konfigurace integrace aplikace Guides ve výrobě")

Nastavte následující pole:

- **Subdoména prostředí CDS** – toto pole by už mělo obsahovat hodnotu. Toto pole obsahuje subdoménu prostředí Common Data Service, ve kterém vytváříte příručky. Tato subdoména je první částí adresy URL a zpravidla je pojmenována po vaší organizaci. Pokud je například vaše adresa URL Common Data Service „contoso.crm4.dynamics.com“, měli byste sem zadat *contoso* . Tato hodnota se používá k vytvoření adres vašich příruček a bude zakódována do kódů QR.
- **Velikost kódu QR** – nastavte velikost vykresleného kódu QR. Doporučujeme zvolit velikost, která vyplní většinu vaší obrazovky, ale ne více. Vhodná hodnota je zpravidla *15* .
- **Úroveň opravy chyb kódu QR** – nastavte členitost kódu QR. Vyšší členitost pomáhá zvýšit spolehlivost kódu, ale **Velikost kódu QR** musí být dostatečně velká, aby podporovala detaily vyžadované vámi vybranou úrovní opravy.


> [!TIP]
> - Kódy QR, které jsou pro váš displej příliš velké, se budou déle vykreslovat a následně se zmenší, aby se vešly na displej. Tím nic nezískáte.
> - Kódy QR, které jsou příliš malé, mohou snížit schopnost HoloLens správně načíst kód v některých prostředích.
> - Doporučujeme otestovat nastavení pro každé zařízení, které bude kódy QR zobrazovat uživatelům HoloLens. Zvolte nastavení, které zajistí dostatečnou čitelnost v prostředí vaší dílny.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Získání přehledu přiřazení všech příruček

Na stránce **Všechny příručky** si můžete prohlédnout seznam všech dostupných příruček ve vaší organizaci a jejich přiřazení k výrobním procesům a prostředkům. Otevřete ji tak, že přejdete na **Hybridní realita \> Příručky \> Všechny příručky** . V horní části seznamu se zobrazují všechny dostupné příručky a pole, které můžete použít k filtrování seznamu. V dolní části seznamu se zobrazují všechna přiřazení příručky a panel nástrojů pro jejich správu.

![Správa příruček](media/instruction-guides-allguides.png "Správa příruček")

V následujících oddílech jsou popsány typy objektů, ke kterým můžete příručky přiřadit. Každá přiřazená příručka obsahuje pokyny, které se automaticky připojí k příslušným výrobním úkolům a budou dostupné v dílně.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Přidružení příručky k prostředku

Přidáním příručky k [prostředku](operations-resources.md) nabídnete tuto příručku v kontextu relevantních výrobních úkolů.

### <a name="typical-scenario-using-resources"></a>Typický scénář využívající prostředky

K nějakému stroji můžete například připojit příručku s obecnými pokyny k obsluze a bezpečnosti práce. Tato příručka pak bude dostupná u každého úkolu, který se na tomto stroji bude provádět.

### <a name="add-a-guide-to-a-resource"></a>Přidání příručky k prostředku

Příručku přidáte k prostředku takto:

1. Přejděte na **Řízení výroby \> Nastavení \> Prostředky \> Prostředky** .
1. V podokně seznamu vyberte prostředek, ke kterému chcete přiřadit příručku.
1. Rozbalte pevnou záložku **Přidružené příručky** .
1. Na panelu nástrojů **Přidružené příručky** vyberte **Přidat** . Do mřížky je přidán nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit. Pokud máte velký počet příruček, můžete filtrováním seznamu najít tu, kterou hledáte.
    ![Správa příruček](media/instruction-guides-allguides.png "Správa příruček")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Přidružení příručky ke skupině prostředků

Příručky můžete přidat ke [skupinám prostředků](tasks/define-discrete-manufacturing-resource-group.md), pokud je používáte ke správě skupin strojů, výrobních linek nebo pracovních buněk.

### <a name="typical-scenarios-using-resource-groups"></a>Typické scénáře využívající skupiny prostředků

**Příklad 1:** Definovali jste skupinu prostředků pro několik strojů stejného modelu. Místo přiřazení příslušné příručky s pokyny k obsluze modelu stroje ke každému příslušnému prostředku byste mohli přiřadit příručku ke skupině prostředků, která obsahuje tento model stroje.

**Příklad 2:** Definovali jste skupinu prostředků pro pracovní buňku, která obsahuje různé stroje, a máte příručku, která poskytuje obecné pokyny pro údržbu této pracovní buňky. Tato příručka platí pro jakoukoli výrobní činnost v této pracovní buňce.

### <a name="add-a-guide-to-a-resource-group"></a>Přidání příručky ke skupině prostředků

Příručku přidáte ke skupině prostředků takto:

1. Přejděte na **Řízení výroby \> Nastavení \> Prostředky \> Skupiny prostředků** .
1. V podokně seznamu vyberte skupinu prostředků, ke které chcete přiřadit příručku.
1. Rozbalte pevnou záložku **Přidružené příručky** .
1. Na panelu nástrojů **Přidružené příručky** vyberte **Přidat** . Do mřížky je přidán nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit. Pokud máte velký počet příruček, můžete filtrováním seznamu najít tu, kterou hledáte.
    ![Přidání příručky ke skupině prostředků](media/instruction-guides-resourcegroup.png "Přidání příručky ke skupině prostředků")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Přidružení příručky k uvolněnému produktu

Příručku můžete přidat k libovolnému [uvolněnému produktu](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Typický scénář využívající uvolněné produkty

Příručky na úrovni produktu poskytují pracovníkům v dílně pokyny týkající se obsluhy nebo manipulace s konkrétním uvolněným produktem nebo položkou.

### <a name="add-a-guide-to-a-released-product"></a>Přidání příručky k uvolněnému produktu

Příručku přidáte k uvolněnému produktu takto:

1. Přejděte na **Řízení informací o výrobě \> Produkty \> Uvolněné produkty** .
1. Otevřete produkt, ke kterému chcete přiřadit příručku.
1. V podokně akcí otevřete kartu **Inženýr** a ve skupině **Zobrazení** vyberte **Přidružené příručky** .
1. Otevře se stránka **Přidružené příručky** pro vybraný produkt.
1. Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky. 
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k uvolněnému produktu](media/instruction-guides-ReleasedProduct-AddGuides.png "Přidání příručky k uvolněnému produktu")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Přidružení příručky k receptuře

Příručku můžete přidat k libovolné [receptuře](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Typický scénář využívající receptury
  
Příručky na úrovni receptury poskytují pracovníkům v dílně pokyny pro manipulaci v kontextu receptury. Příručky lze přiřadit rovněž k verzím receptury.

> [!NOTE]
> Pokyny relevantní pro výrobní procesy založené na receptuře můžete přiřadit k postupu, verzi postupu nebo vztahům operací postupu.  

> Příručky nelze momentálně připojit k jednotlivým řádkům receptury.

### <a name="add-a-guide-to-a-formula"></a>Přidání příručky k receptuře

Příručku přidáte k receptuře takto:

1. Přejděte na **Řízení informací o produktech \> Kusovníky a receptury \> Receptury** .
1. Otevřete recepturu, ke které chcete přiřadit příručku.
1. Otevřete kartu **Záhlaví** nad horní pevnou záložkou.
1. Rozbalte pevnou záložku **Přidružené příručky** .
1. Na panelu nástrojů **Přidružené příručky** vyberte **Přidat** . Do mřížky je přidán nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k receptuře](media/instruction-guides-Formula.png "Přidání příručky k receptuře")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Přidružení příručky k verzi receptury

Příručku můžete přidat k libovolné [verzi receptury](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Typický scénář využívající verze receptury

Příručky připojené k individuální verzi receptury poskytují pracovníkům v dílně pokyny, které vysvětlují výrobu dané verze receptury.

> [!TIP]
> Pokyny relevantní pro výrobní procesy založené na této verzi receptury můžete přiřadit k postupu, verzi postupu nebo vztahům operací postupu.  

> [!NOTE]
> Příručky nelze momentálně připojit k jednotlivým řádkům receptury.

### <a name="add-a-guide-to-a-formula-version"></a>Přidání příručky k verzi receptury

Příručku přidáte k verzi receptury takto:

1. Přejděte na **Řízení informací o produktech \> Kusovníky a receptury \> Receptury** .
1. Otevřete recepturu obsahující verzi, ke které chcete přiřadit příručku.
1. Otevřete kartu **Záhlaví** nad horní pevnou záložkou.
1. Na pevné záložce **Verze receptury** vyberte verzi, ke které chcete přiřadit příručku.
1. Na panelu nástrojů **Verze receptury** vyberte **Přidružené příručky** .
    ![Otevření příruček přidružených k vybrané verzi receptury](media/instruction-guides-FormulaVersion.png "Otevření příruček přidružených k vybrané verzi receptury")
1. Otevře se stránka **Přidružené příručky** pro verzi receptury.
1. Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky. 
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k verzi receptury](media/instruction-guides-FormulaVersionAddGuide.png "Přidání příručky k verzi receptury")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Přidružení příručky ke kusovníku

Příručku můžete přidat k libovolnému [kusovníku](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Typický scénář využívající kusovníky

Příručky připojené ke kusovníku poskytují pracovníkům v dílně pokyny, které vysvětlují, jak připravit a zacházet s materiálem z kusovníku. Příručky lze přiřadit rovněž k verzím kusovníku.

> [!NOTE]
> Příručky nelze momentálně připojit k jednotlivým řádkům kusovníku.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Přidání příručky ke kusovníku

Příručku přidáte ke kusovníku takto:

1. Přejděte na **Řízení informací o výrobě \> Kusovníky a receptury \> Kusovníky** .
1. Otevřete kusovník, ke kterému chcete přiřadit příručku.
1. Otevřete kartu **Záhlaví** nad horní pevnou záložkou.
1. Rozbalte pevnou záložku **Přidružené příručky** .
1. Na panelu nástrojů **Přidružené příručky** vyberte **Přidat** . Do mřížky je přidán nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky ke kusovníku](media/instruction-guides-BOM.png "Přidání příručky ke kusovníku")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Přidružení příručky k verzi kusovníku

Příručku můžete přidat k libovolné [verzi kusovníku](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Typický scénář využívající verze kusovníku

Příručky připojené k individuální verzi kusovníku poskytují pracovníkům v dílně pokyny, které vysvětlují, jak připravit a zacházet s materiálem pro verzi kusovníku, která se liší od obecného kusovníku nebo jeho jiných verzí.

> [!NOTE]
> Příručky nelze momentálně připojit k jednotlivým řádkům kusovníku.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Přidání příručky k verzi kusovníku

Příručku přidáte k verzi kusovníku takto:

1. Přejděte na **Řízení informací o výrobě \> Kusovníky a receptury \> Kusovníky** .
1. Otevřete kusovník obsahující verzi, ke které chcete přiřadit příručku.
1. Otevřete kartu **Záhlaví** nad horní pevnou záložkou.
1. Na pevné záložce **Verze kusovníku** vyberte verzi, ke které chcete přiřadit příručku.
1. Na panelu nástrojů **Verze kusovníku** vyberte **Přidružené příručky** .
    ![Otevření příruček přidružených k vybrané verzi kusovníku](media/instruction-guides-BOMVersion.png "Otevření příruček přidružených k vybrané verzi kusovníku")
1. Otevře se stránka **Přidružené příručky** pro verzi kusovníku.
1. Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k verzi kusovníku](media/instruction-guides-BOMVersionAddGuide.png "Přidání příručky k verzi kusovníku")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Přidružení příručky k postupu

Příručku můžete přidat k libovolnému [postupu](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Typický scénář využívající postupy

Pomocí postupů se zpravidla určuje, jak se má vyrobit určitý uvolněný produkt na základě kusovníku nebo verze kusovníku a se sadou prostředků nebo skupinami prostředků.

Přiřazením příručky k postupu poskytnete podrobné pokyny pro příslušný výrobní proces.

### <a name="add-a-guide-to-a-route"></a>Přidání příručky k postupu

Příručku přidáte k postupu takto:

1. Přejděte na **Řízení výroby \> Všechny postupy** .
1. Otevřete postup, ke kterému chcete přiřadit příručku.
1. Rozbalte pevnou záložku **Přidružené příručky** .
1. Na panelu nástrojů **Přidružené příručky** vyberte **Přidat** . Do mřížky je přidán nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k postupu](media/instruction-guides-Route.png "Přidání příručky k postupu")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Přidružení příručky k verzi postupu

Příručku můžete přidat k libovolné [verzi postupu](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Typický scénář využívající verze postupu

Verze postupů se obvykle používají k určení variant výrobních procesů založených na existujícím postupu. Ke každé verzi postupu můžete přiřadit odlišné příručky.

### <a name="add-a-guide-to-a-route-version"></a>Přidání příručky k verzi postupu

Příručku přidáte k verzi postupu takto:

1. Přejděte na **Řízení výroby \> Všechny postupy** .
1. Otevřete postup, ke kterému chcete přiřadit příručku.
1. Na pevné záložce **Verze** vyberte verzi, ke které chcete přiřadit příručku.
1. Na panelu nástrojů **Verze** vyberte **Přidružené příručky** .
    ![Otevření příruček přidružených k vybrané verzi postupu](media/instruction-guides-RouteVersion.png "Otevření příruček přidružených k vybrané verzi postupu")
1. Otevře se stránka **Přidružené příručky** pro verzi kusovníku.
1. Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.
    ![Přidání příručky k verzi postupu](media/instruction-guides-RouteVersionAddGuide.png "Přidání příručky k verzi postupu")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Přidružení příručky ke vztahu operace postupu

Příručku můžete přidat k libovolnému [vztahu operace postupu](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Typický scénář využívající vztahy operací postupu

Vztahy operací představují nejkonkrétnější způsob přidání pokynů k procesu produktu a jeho souvisejícím operacím. Můžete zadat pokyny pro každou operaci postupu a odlišné pokyny pro jakýkoli typ kontextu vztahu určený pro postup, například pro konkrétní položky, konfigurace a další. Můžete rovněž určit, na které fáze operace se tyto pokyny vztahují (například nastavení, řazení do fronty, zpracování nebo dopravu).

> [!NOTE]
> Pokud zadáte příručky pro několik vztahů operací postupu, zobrazí se v dílně pro vygenerovaný úkol jen příručka z nejkonkrétnějšího vztahu.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Přidání příručky ke vztahu operace postupu

Příručku přidáte ke vztahu operace postupu takto:

1. Přejděte na **Řízení výroby \> Všechny postupy** .
1. Otevřete postup, ke kterému chcete přiřadit příručku.
1. V podokně akcí otevřete kartu **Postup** a ve skupině **Údržba** vyberte **Podrobnosti postupu** .
1. Otevře se stránka **Podrobnosti postupu** pro vybraný postup.
1. V horní mřížce vyberte operaci, ke které chcete poskytnout pokyny.
1. V dolní mřížce vyberte konkrétní vztah (nebo obecný vztah **Vše** ).
    ![Výběr operace a následně vztahu](media/instruction-guides-RouteOperationRelation.png "Výběr operace a následně vztahu")
1. Nad dolní mřížkou otevřete kartu **Přidružené příručky** . ![Karta Přidružené příručky](media/instruction-guides-RouteOperationRelation-AddGuide.png "Karta Přidružené příručky")
1. Výběrem možnosti **Přidat** na panelu nástrojů v horní části dolní mřížky přidejte do mřížky nový řádek.
1. Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit. Ve zbytku řádku zaškrtněte políčko pro každý kontext, ve kterém má být vybraná příručka dostupná.

> [!NOTE]
> Pro každou fázi jednotlivých operací můžete přidat jednu nebo více příruček.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Výběr příruček z realizačního rozhraní dílny

Když si pracovník otevře v realizačním rozhraní dílny seznam úkolů, najde Supply Chain Management příslušné příručky pro zobrazené úkoly. Tlačítkem **Příručky** si zobrazí relevantní příručky.

![Tlačítko Příručky v realizačním rozhraní dílny](media/instruction-guides-Shopfloor1.png "Tlačítko Příručky v realizačním rozhraní dílny")

Pak si nasadí HoloLens a zpřístupní příslušnou příručku pohledem na kód QR a aktivací příslušné příručky.

![Kód QR pro přístup k příručce pomocí HoloLens](media/instruction-guides-Shopfloor2.png "Kód QR pro přístup k příručce pomocí HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Logika pro výběr příruček

Příručky můžete přidat k následujícím výrobním datům:

- [Prostředky](#resources)
- [Skupiny prostředků](#resource-groups)
- [Uvolněné produkty](#released-products)
- [Receptury](#formulas)
- [Verze receptury](#formula-versions)
- [Kusovníky](#bom)
- [Verze kusovníků](#bom-versions)
- [Postupy](#routes)
- [Verze postupu](#route-versions)
- [Vztahy operací postupu](#route-operation-relations)

Když Supply Chain Management vygeneruje úkoly pro výrobu, shromáždí z těchto zdrojů příslušné příručky. Vezměte na vědomí následující důležitá pravidla.

- Pokud připojíte verzi kusovníku nebo verzi receptury k postupu nebo výrobní zakázce, zobrazí se u úkolu všechny příručky připojené k této verzi a také příručky připojené k nadřazenému kusovníku nebo receptuře této verze.
- Pokud připojíte verzi postupu k výrobní zakázce, zobrazí se u úkolu všechny příručky připojené k této verzi a také příručky připojené k nadřazenému postupu této verze.
- Pokud definujete několik vztahů operací postupu, které obsahují vztah *Vše* , a přiřadíte k nim příručky, zobrazí se u úkolu jen příručky z nejkonkrétnějšího vztahu.  

![Schéma řešení relevantních příruček](media/instruction-guides-Resolve.png "Schéma řešení relevantních příruček")
