---
title: Ukázka funkce správy technických změn
description: Tento článek poskytuje podrobný návod, který ukazuje, jak pracovat se správou technických změn.
author: t-benebo
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 65ff30632a54b0b7cadbfe663698d466d41abe47
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334888"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Ukázka funkce správy technických změn

[!include [banner](../includes/banner.md)]

Tento článek poskytuje podrobný návod, který ukazuje, jak pracovat se správou technických změn. Prochází každý z nejdůležitějších scénářů:

- Konfigurace základních funkcí
- Jak technická společnost vytváří nový technický produkt
- Jak technická společnost vydává technický produkt místní společnosti
- Jak může místní společnost zkontrolovat a přijmout produkt, který jí byl vydán technickou společností
- Jak může místní společnost používat technický produkt ve standardních transakcích
- Jak přidat technický produkt k prodejní objednávce
- Jak požádat o změny technického produktu vytvořením požadavku na technické změny
- Jak naplánovat a implementovat požadované změny vytvořením objednávky technických změn
- Jak uvolnit produkt, který byl změněn

Všechna cvičení v tomto článku používají standardní ukázková data, která jsou k dispozici pro Microsoft Dynamics 365 Supply Chain Management. Každé cvičení navazuje na předchozí cvičení. Proto doporučujeme, abyste prošli cvičeními v pořadí, od začátku do konce, zejména pokud jste nikdy předtím nepoužívali funkci správy technických změn. Tímto způsobem získáte úplné pochopení funkce.

## <a name="set-up-for-the-sample-scenario"></a>Nastavení ukázkových dat pro tento scénář

Chcete-li sledovat ukázkový scénář, který je uveden v tomto článku, musíte nejprve připravit funkci zpřístupněním ukázkových dat a přidáním několika vlastních záznamů.

Než se pokusíte provést některá z cvičení ve zbytku tohoto článku, postupujte podle pokynů ve všech následujících podsekcích. Tyto podsekce také představují několik důležitých stránek nastavení, které budete používat při nastavování správy technických změn pro vaši vlastní organizaci.

### <a name="make-standard-demo-data-available"></a>Zpřístupnění standardních ukázkových dat

Pracujte na systému, kde jsou nainstalována standardní [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md). Standardní ukázková data přidávají data pro několik ukázkových právnických osob (společností a organizací). Během cvičení budete přepínat mezi jednou společností pomocí nástroje pro výběr společnosti na pravé straně navigačního panelu (*DEMF*), který je nastaven jako *technická organizace* a další společnost (*USMF*), který je nastaven jako *provozní organizace*.

### <a name="set-up-an-engineering-organization"></a>Vytvoření technické organizace

Technická organizace vlastní technická data a odpovídá za design produktu a jeho změny. Chcete-li nastavit technické organizace, postupujte následujícím způsobem.

1. Jděte na **Správa technických změn &gt; Nastavení &gt; Technické atributy**.
1. Vyberte **Nový** pro přidání řádku do mřížky a pak pro něho nastavte tyto hodnoty:

    - **Technická organizace:** *DEMF*
    - **Název organizace:** *Contoso Entertainment System Germany*

    ![Přidání technické organizace.](media/engineering-org.png "Přidání technické organizace")

### <a name="set-up-the-version-product-dimension-group"></a>Nastavení skupiny dimenzí produktu verze

1. Přejděte na **Správa informací o produktu &gt; Nastavení &gt; Rozměry a skupiny variant &gt; Skupiny dimenzí produktu**.
1. Vyberte **Nový** pro vytvoření skupiny dimenzí produktu.
1. Nastavte pole **Název** na *Verze*.
1. Vyberte **Uložit** pro uložení nové dimenze a načtení hodnot na pevné záložce **Dimenze produktu**.
1. Na pevné záložce **Dimenze produktu** nastavte jako aktivní dimenzi produktu **Verze**.

    ![Přidání skupiny sledovací dimenze produktů.](media/product-dimension-groups.png "Přidání skupiny sledovací dimenze produktů")

### <a name="set-up-product-lifecycle-states"></a>Nastavení stavů životního cyklu produktu

Protože technický produkt prochází svým životním cyklem, je důležité, abyste mohli kontrolovat, které transakce jsou povoleny pro každý stav životního cyklu. Chcete-li nastavit stavy životního cyklu produktu, postupujte následujícím způsobem.

1. Jděte na **Správa technických změn &gt; Nastavení &gt; Stav životního cyklu produktu**.
1. Vyberte **Nový** pro přidání stavu životního cyklu a pak pro něho nastavte tyto hodnoty:

    - **Stav:** *provozní*
    - **Popis:** *Provozní*

1. Vyberte **Uložit** pro uložení nového stavu životního cyklu a načtení hodnot na pevné záložce **Povolené obchodní procesy**.
1. Na pevné záložce **Povolené obchodní procesy** vyberte obchodní procesy, které by měly být k dispozici. U tohoto příkladu ponechte pole **Zásady** nastavené na *Povoleno* pro všechny obchodní procesy.

    ![Povolení obchodních procesů pro stav životního cyklu.](media/product-lifecycle-states-1.png "Povolení obchodních procesů pro stav životního cyklu")

1. Vyberte **Nový** pro přidání dalšího stavu životního cyklu a pak pro něho nastavte tyto hodnoty:

    - **Stav:** *Prototyp*
    - **Popis:** *Prototyp*

1. Vyberte **Uložit** pro uložení nového stavu životního cyklu a načtení hodnot na pevné záložce **Povolené obchodní procesy**.
1. Na pevné záložce **Povolené obchodní procesy** vyberte obchodní procesy, které by měly být k dispozici. U tohoto příkladu nastavte pole **Zásady** nastavené na *Povoleno s varováním* pro všechny obchodní procesy.

    ![Povolení (s varováním) obchodních procesů pro stav životního cyklu.](media/product-lifecycle-states-2.png "Povolení (s varováním) obchodních procesů pro stav životního cyklu")

### <a name="set-up-a-version-number-rule"></a>Nastavení pravidla čísla verze

1. Jděte na **Správa technických změn &gt; Nastavení &gt; Pravidlo čísla verze**.
1. Vyberte **Nový** pro přidání pravidla a pak pro něho nastavte tyto hodnoty:

    - **Název:** *Auto*
    - **Číslo pravidla:** *Auto*
    - **Formát:** *V-\#\#*

    ![Přidání pravidla pro číslo verze produktu.](media/version-number-rule.png "Přidání pravidla pro číslo verze produktu")

### <a name="set-up-a-product-release-policy"></a>Nastavení zásad vydání produktu

1. Jděte na **Správa technických změn &gt; Nastavení &gt; Zásady vydání produktu**.
1. Vyberte **Nový** pro přidání zásad vydání a pak pro ně nastavte tyto hodnoty:

    - **Název:** *Součásti*
    - **Popis:** *Součásti*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Typ produktu:** *Položka*
    - **Použít šablony:** *Vždy*
    - **Aktivní:** *Ano*

1. Na pevné záložce **Všechny produkty** vyberte **Přidat**, chcete-li přidat řádek a poté pro něj nastavit následující hodnoty:

    - **Společnost:** *DEMF*
    - **Šablona vydaného produktu:** *D0006*

1. Chcete-li přidat další řádek, klikněte znovu na **Přidat** a zadejte následující hodnoty:

    - **ID účtů společnosti:** *USMF*
    - **Šablona vydaného produktu:** *D0006*
    - **Přijímající kusovník:** Zaškrtněte toto políčko.
    - **Kopírovat schválení kusovníku:** Zaškrtněte toto políčko.
    - **Kopírovat aktivaci kusovníku:** Zaškrtněte toto políčko.
    - **Přijímající trasa:** Zaškrtněte toto políčko.
    - **Kopírovat schválení trasy:** Zaškrtněte toto políčko.
    - **Aktivace schválení trasy:** Zaškrtněte toto políčko.

    ![Přidání zásad vydání produktu.](media/product-release-policy.png "Přidání zásad vydání produktu")

### <a name="set-up-an-engineering-product-category"></a>Nastavení kategorií technického produktu 

Kategorie technických produktů poskytují základ pro vytváření technických produktů (tj. produktů, jejichž verze a verze jsou řízeny prostřednictvím správy technických změn). Chcete-li nastavit kategorie produktu, postupujte následujícím způsobem.

1. Jděte na **Správa technických změn &gt; Podrobnosti kategorie technického produktu**.
1. Chcete-li vytvořit kategorii, klikněte na **Nová**.
1. Na pevné záložce **Obecné** nastavte následující hodnoty:

    - **Název:** *Součásti*
    - **Technická organizace:** *DEMF*
    - **Typ produktu:** *Položka*
    - **Sledování verzí v transakcích:** *Ano*
    - **Skupina dimenzí produktů:** *Verze*
    - **Stav životního cyklu produktu při vytvoření:** *Provozní*
    - **Pravidlo čísla verze:** *Auto*
    - **Vynutit účinnost:** *Ne*
    - **Použít nomenklaturu pravidla počtu:** *Ne*
    - **Použít nomenklaturu pravidla názvu:** *Ne*
    - **Použít nomenklaturu pravidla popisu:** *Ne*

1. Na pevné záložce **Zásady vydání** nastavte hodnotu v poli **Zásady vydání produktu** na *Komponenty*.
1. Zvolte možnost **Uložit**.

    ![Přidání kategorií technického produktu.](media/product-category-details.png "Přidání kategorií technického produktu")

### <a name="set-up-product-acceptance-conditions"></a>Nastavení podmínek přijetí produktu

1. Pomocí nástroje pro výběr společnosti na pravé straně navigační lišty přepněte na ikonu právnické osoby *USMF* (společnost).
1. Jděte na **Správa technických změn &gt; Nastavení &gt; Parametry správy technické změny**.
1. Na kartě **Kontrola vydání** v části **Přijetí produktu** nastavte pole **Přijetí produktu** na *Ruční*.

    ![Nastavení podmínek přijetí produktu.](media/engineering-change-management-parameters.png "Nastavení podmínek přijetí produktu")

## <a name="create-a-new-engineering-product"></a>Vytvoření nového technického produktu

Technický produkt je produkt, který má verzi a je řízen prostřednictvím řízení technických změn. Jinými slovy, můžete řídit změny během jeho životnosti a informace o změnách se uloží pomocí technických změnových příkazů. Při vytváření technických produktů postupujte takto.

1. Ujistěte se, že jste v právnické osobě vaší technické organizace (*DEMF* pro tento příklad). Podle potřeby použijte výběr společnosti na pravé straně navigační lišty.
1. Otevřete stránku **Vydané produkty** pomocí jednoho z následujících kroků:

    - Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.
    - Jděte na **Správa technických změn &gt; Společné &gt; Vydané produkty**.

1. V podokně akcí na kartě **Produkt** ve skupině **Nový** zvolte **Technický produkt**.
1. V dialogovém okně **Nový produkt** nastavte následující hodnoty:

    - **Kategorie technického produktu:** *Komponenty*
    - **Číslo produktu:** *Z0001*
    - **Název produktu:** *Sada reproduktorů*

    ![Přidání technického produktu.](media/new-product-dialog.png "Přidání technického produktu")

    Všimněte si, že pole **Verze** se automaticky nastavuje pomocí pravidla čísla produktu, které jste nastavili dříve.

1. Vyberte **OK**, produkt se vytvoří a dialogové okno se zavře.
1. Otevře se stránka s podrobnostmi o novém produktu. Všimněte si, že hodnoty jsou již vyplněny pro některá pole, například **Skupina dimenzí úložiště**, **Sledování skupiny dimenzí** a/nebo **Skupina modelů položek**. Tato pole byla nastavena automaticky, protože produkt je vydáván v právnické osobě *DEMF* a používá zásady uvolnění produktu *Komponenty*, která je spojena s kategorií technických produktů *Komponenty*. Protože jste dříve používali položku *D0006* jako šablonu pro nastavení řádku pro právnickou osobu *DEMF*, hodnoty, které byly vyplněny, byly převzaty z položky *D0006*.

    ![Podrobnosti o uvolněném produktu.](media/product-details.png "Podrobnosti o uvolněném produktu")

1. V podokně akcí na kartě **Technik** ve skupině **Správa technických změn** vyberte **Technické verze** k zobrazení verzí produktu.

    ![Technické verze.](media/engineering-versions-list.png "Technické verze")

1. Na stránce **Technické** si všimněte si, že pro produkt existuje pouze jedna verze a je aktivní.
1. Vyberte verzi, jejíž podrobnosti chcete zobrazit.

    ![Podrobnosti o technické verzi.](media/engineering-version-details.png "Podrobnosti o technické verzi")

1. Na stránce **Technická verze** na pevné záložce **Kusovník** vyberte **Vytvořit kusovník**.
1. V dialogovém okně **Vytvořit kusovník** nastavte následující hodnoty:

    - **Číslo kusovníku:** Z0001
    - **Název:** Sada reproduktorů
    - **Lokalita:** 1

    ![Vytváření BOM.](media/create-bom.png "Vytváření BOM")

1. Vyberte **OK** pro přidání kusovníku a zavření dialogového okna.
1. Na pevné záložce **Kusovník** vyberte **Kusovník**.
1. Na stránce **Kusovník** na pevné záložce **Řádky kusovníku** přidejte tři řádky pro čísla položek *D0001*, *D0003*, a *D0006*.

    ![Přidávání řádků kusovníku.](media/bom.png "Přidávání řádků kusovníku")

1. Zvolte možnost **Uložit**.
1. Zavřete stránku.
1. Na stránce **Technická verze** na pevné záložce **Kusovník** vyberte **Schválit**.
1. V zobrazeném dialogovém okně vyberte **OK**.

    ![Schvalování kusovníku.](media/approve-dialog.png "Schvalování kusovníku")

1. Na stránce **Technická verze** na pevné záložce **Kusovník** vyberte **Aktivovat**.
1. Všimněte si, že jsou pro kusovník zaškrtnutá políčka **Aktivní** a **Schválený**.

    ![Aktivní a schválený kusovník.](media/approved-bom.png "Aktivní a schválený kusovník")

1. Zavřete stránku.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Vydání technického produktu místní společnosti

Produkt nyní navrhlo technické oddělení. V tomto příkladu je produkt prototypem, který technické oddělení navrhlo pro zákazníka. Protože zákazník je zákazníkem právnické osoby *USMF*, produkt musí být této právnické osobě vydán.

1. Nechte právnickou osobu nastavenou na *DEMF*. (Podle potřeby použijte výběr společnosti na pravé straně navigační lišty.)
1. Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.
1. Vyberte produkt *Z0001*.
1. V podokně akcí na kartě **Produkt** ve skupině **Správa** vyberte **Struktura vydání produktu** k otevření průvodce **Vydání produktů**.
1. Na stránce **Vyberte technické produkty, které chcete vydat** zaškrtněte políčko **Vybrat** u produktu *Z0001*.

    ![Výběr technických produktů k vydání.](media/select-eng-product-to-release.png "Výběr technických produktů k vydání")

1. Vyberte **Podrobnosti o vydání**.
1. Zobrazí se stránka **Podrobnosti o vydání produktu**, kde si můžete prohlédnout podrobnosti o produktu, který bude vydán, a jeho strukturu produktu. Všimněte si, že je možnost **Odeslat kusovník** nastavena na hodnotu *Ano*. Proto budou vydány jak produkt *Z0001*, tak všechny jeho podřízené položky z kusovníku.

    V levém podokně můžete vybrat libovolnou podřízenou položku a zkontrolovat její podrobnosti. Pokud má některá podřízená položka kusovník, můžete také vybrat vydání kusovníku této podřízené položky.

    ![Kontrola podrobností o vydání produktu.](media/product-release-details.png "Kontrola podrobností o vydání produktu")

1. Zavřete stránku a vraťte se do průvodce **Vydané produkty**.
1. Výběrem **Další** otevřete stránku **Vybrat produkty k vydání**. Pokud jste vybrali nějaké standardní (netechnické) produkty, zobrazí se na této stránce. Upozorňujeme, že když vydáte standardní produkt výběrem **Vydat strukturu produktu**, vydá se také jeho kusovník a trasa.

    ![Výběr standardních produktů k vydání.](media/select-std-product-to-release.png "Výběr standardních produktů k vydání")

1. Výběrem **Další** otevřete stránku **Vybrat varianty produktu k vydání**. V tomto příkladu nejsou žádné varianty.
1. Výběrem **Další** otevřete stránku **Vybrat společnosti**.
1. Vyberte společnosti, kterým by měl být produkt vydán. V tomto příkladu zaškrtněte políčko **USMF**.

    ![Výběr společností, kterým se má produkt vydat.](media/select-release-companies.png "Výběr společností, kterým se má produkt vydat")

1. Výběrem **Další** otevřete stránku **Potvrdit výběr**.
1. Vyberte **Dokončit**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Než produkt vydáte v místní společnosti, zkontrolujte jej a přijměte

Technické oddělení nyní zveřejnilo informace místním společnostem, kde bude produkt používán. V tomto příkladu je místní společnost *USMF*.

Protože jste nastavili pole **Přijetí produktu** na *Ruční* na stránce **Parametry řízení technických změn** pro společnost *USMF*, musí být produkty před vydáním ručně přijaty. Jinými slovy, musí být zkontrolovány a přijaty dříve, než se stanou vydanými produkty.

Pokud chcete produkt zkontrolovat a vydat společnosti *USMF*, postupujte podle těchto kroků.

1. Nastavte právnickou osobu na *USMF*. (Použijte výběr společnosti na pravé straně navigační lišty.)
1. Jděte na **Správa technické změny &gt; Společné &gt; Vydání produktu &gt; Otevřít vydání produktu**.

    Na stránce **Otevřít vydání produktu** se zobrazuje produkt *Z0001*, který má stav *Čeká na přijetí*.

    ![Otevřená uvolnění produktů.](media/open-product-releases.png "Otevřená uvolnění produktů")

1. Vyberte hodnotu ve sloupci **Číslo produktu** k otevření stránky **Podrobnosti o vydání produktu**. Všímejte si následujících podrobností:

    - Na pevné záložce **Obecné** se zobrazují informace o vydání produktu, například vydávající společnost (*DEMF* v tomto příkladu), vydávající pracoviště (*1*) a přijímající pracoviště (*1*). Protože jste nezadali přijímající pracoviště v průvodci **Vydat produkty**, hodnota vydávajícího pracoviště se zkopíruje na přijímající pracoviště.
    - Na pevné záložce **Podrobnosti o vydání** se zobrazují informace o produktu a verzi, které byly vydány. Zde můžete upravit nastavení, například data účinnosti.
    - Na pevné záložce **Trasa** se zobrazuje trasa produktu. V tomto příkladu jste však nevydali žádné trasy.

    ![Podrobnosti o uvolnění produktu.](media/product-release-details-2.png "Podrobnosti o uvolnění produktu")

1. Po dokončení kontroly informací jste připraveni produkt přijmout a tímto způsobem jej vydat společnosti *USMF*. V podokně akcí klikněte na **Akce &gt; Přijmout**.
1. Produkt je nyní vydán společnosti *USMF*. Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**. Měli byste vidět položku *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Použití produktu v transakcích v místní společnosti

Správce kmenových dat pro společnost *USMF* chce zajistit, aby byl produkt ve stavu *Prototyp* stavu, aby bylo zajištěno, že uživatelé budou varováni, pokud jej omylem přidají do procesů, na kterých pracují.

1. Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.
1. Vyberte produkt *Z0001*, aby se otevřela jeho stránka s podrobnostmi. (K vyhledání produktu můžete použít filtr.)
1. V podokně akcí na kartě **Technik** ve skupině **Správa technických změn** vyberte **Technické verze**.
1. Na stránce **Technické verze** vyberte číslo verze *V-01* k otevření její stránky s podrobnostmi.
1. V podokně akcí na kartě **Produkt** ve skupině **Stav životního cyklu** vyberte **Změnit stav životního cyklu**.
1. V rozevíracím dialogovém okně **Změnit stav životního cyklu** nastavte pole **Stav** na *Prototyp* a potom vyberte **OK**.

    ![Změna stavu životního cyklu.](media/change-lifecycle-state.png "Změna stavu životního cyklu")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Přidání technického produktu k prodejní objednávce

Produkt lze nyní prodat zákazníkovi. Pro přidání produktu do prodejní objednávky postupujte následovně.

1. Přejděte na **Prodej a marketing &gt; Prodejní objednávky &gt; Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvořit prodejní objednávku** nastavte pole **Zákaznický účet** na *US-0002* a vyberte **OK**.
1. Otevře se nová prodejní objednávka. Na pevné záložce **Řádky prodejní objednávky** přidejte řádek a nastavte pro něho pole **Číslo položky** na *Z000*.
1. V podokně akcí vyberte **Uložit**.

    Zobrazí se varovná zpráva, která vás informuje, že položka má stav *Prototyp*. Protože je však zpráva pouze upozorněním, byla prodejní objednávka přesto vytvořena.

    ![Prodejní objednávka pro technický produkt.](media/sales-order-eng-product.png "Prodejní objednávka pro technický produkt")

## <a name="request-changes-in-the-engineering-product"></a>Vyžádání změn v technickém produktu

Produkt byl odeslán zákazníkovi, ale zákazník nebyl zcela spokojen a poskytuje zpětnou vazbu, která obsahuje návrhy na zlepšení. Zatímco zákazník hovoří s prodavačem po telefonu, může prodavač požadovat změny, které zákazník popisuje.

1. Přejděte na **Prodej a marketing &gt; Prodejní objednávky &gt; Všechny prodejní objednávky**.
1. Najděte a otevřete prodejní objednávku, kterou jste vytvořili v předchozím cvičení.
1. Na pevné záložce **Řádky prodejní objednávky** vyberte **Správa technických změn &gt; Nová žádost o technickou změnu**.

    ![Vytvoření požadavku na technickou změnu z prodejní objednávky.](media/sales-order-eng-change-request.png "Vytvoření požadavku na technickou změnu z prodejní objednávky")

1. Vyplňte požadavek na technickou změnu na základě zpětné vazby od zákazníka. Pro tento příklad nastavte následující hodnoty:

    - **Žádost o změnu:** *555*
    - **Název:** *Změna zákazníka Z0001*
    - **Priorita:** *nízká*
    - **Kategorie:** nastavit změnu
    - **Vážnost:** *střední*

1. Na pevné záložce **Informace** vyberte **Nová &gt; Poznámka** pro přidání poznámky do mřížky.
1. V poli **Popis** pro novou poznámku označte, že by položka *D0003* měla být z kusovníku odstraněna. Pokud k poznámce musíte přidat další informace, můžete zadat text do pole **Poznámky**.

    ![Požadavek na technickou změnu.](media/eng-change-request.png "Požadavek na technickou změnu")

1. V podokně akcí vyberte **Uložit**.
1. Všimněte si, že položka byla automaticky přidána na pevnou záložku **Produkty** a že zdroj požadavku na technickou změnu (prodejní objednávka) byl přidán na pevnou záložku **Zdroj**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Proveďte změny v produktu pomocí objednávky technických změn

Prodavač ví, že produkt je důležitý a byl navržen speciálně pro zákazníka. Proto prodavač volá inženýra ve společnosti *DEMF*, aby ho informoval o požadavku na změnu. Tímto způsobem může technik urychlit proces.

Technik nyní zkontroluje požadavek od zákazníka a vytvoří objednávku změny produktu.

1. Protože technik pracuje ve společnosti *DEMF*, nastavte právnickou osobu na *DEMF*. (Použijte výběr společnosti na pravé straně navigační lišty.)
1. Přejděte na Správa technických změn **Společné &gt; Správa technických změn &gt; Požadavky na technickou změnu**.
1. Otevřete žádost o změnu *555*.
1. Zkontrolujte informace a poté změnu schvalte. V podokně akcí na kartě **Požadavek na změnu** ve skupině **Změnit stav** vyberte **Schválit**.
1. Přejděte na Správa technických změn **Společné &gt; Správa technických změn &gt; Příkazy technické změny**.
1. V podokně akcí vyberte **Nový** k vytvoření typu příkazu změny a nastavte pro něj následující hodnoty:

    - **Příkaz ke změně:** *555*
    - **Název:** *Změna zákazníka Z0001*
    - **Kategorie:** *Změna zákazníka*
    - **Priorita:** *nízká*
    - **Vážnost:** *střední*

1. Na pevné záložce **Ovlivněné produkty** vyberte **Nový &gt; Přidat technický produkt** pro přidání řádku do mřížky a nastavte pro něho následující hodnoty:

    - **Produkt:** *Z0001*
    - **Dopad:** *Nová verze*

    ![Vytvoření objednávky technických změn.](media/eng-change-order.png "Vytvoření objednávky technických změn")

1. Všimněte si toho, protože jste nastavili pole **Dopad** na *Nová verze*, pole **Nová verze** na kartě **Detaily** na pevné záložce **Detaily produktu** ukazuje, jaké bude nové číslo verze (*V-02* pro tento příklad).

    ![Podrobnosti o produktu pro technický změnový příkaz.](media/eng-change-order-product-details.png "Podrobnosti o produktu pro technický změnový příkaz")

1. V podokně akcí vyberte **Uložit**.
1. Na pevné záložce **Podrobnosti o produktu** na kartě **Kusovník** vyberte **Řádky** k otevření verze kusovníku *V-01* produktu *Z0001*.

    ![Řádky kusovníku technického produktu.](media/eng-product-bom-lines.png "Řádky kusovníku technického produktu")

1. Vyberte řádek s číslem položky *D0003* a poté v podokně akcí vyberte **Odstranit**. Hodnota pole **Změnit typ** pro tento řádek se změní na *Smazáno*.
1. V podokně akcí vyberte **Uložit**.

    ![Změněné řádky kusovníku technického produktu.](media/eng-product-bom-lines-modified.png "Změněné řádky kusovníku technického produktu")

1. Zavřete stránku **Řádek kusovníku** pro návrat na stránku **Pořadí technických změn**.
1. Na pevné záložce **Podrobnosti o produktu** na kartě **Kusovník** si všimněte, že hodnota pole **Typ změny** pro kusovník *Z0001* je nyní *Změněno*.

    ![Pořadí technických změn, které obsahuje změněný kusovník.](media/eng-change-order-changed-bom.png "Pořadí technických změn, které obsahuje změněný kusovník")

    Nákupní objednávka musí být nyní schválena, než bude možné zpracovat změny. Když jsou změny zpracovány, produkty se aktualizují o změny, které jsou zahrnuty v pořadí technických změn. V tomto příkladu byla osoba, která vytvoří objednávku technické změny, zadána jako schvalovatel.

1. V podokně akcí na kartě **Příkaz ke změně** ve skupině **Změnit stav** vyberte **Schválit**.
1. Vyberte **Proces** k aktualizaci informací o produktu.

## <a name="release-the-changed-product"></a>Vydání změněného produktu

Produkt lze nyní znovu vydat do společnosti *USMF* a poté odeslat zákazníkovi. Chcete-li produkt vydat přímo z objednávky technických změn, postupujte takto.

1. Otevřete pořadí technických změn, které jste vytvořili v předchozím cvičení, pokud ještě není otevřené.
1. V podokně akcí na kartě **Příkaz ke změně** ve skupině **Vydání produktu** vyberte **Vyhledat**.
1. Výsledky hledání ukazují, kterým společnostem byly dotčené produkty vydány. Zavřete výsledky hledání.
1. V podokně akcí na kartě **Změnit objednávku** ve skupině **Vydání produktu** vyberte **Zobrazení** k otevření dialogového okna **Vydání**, kde si můžete prohlédnout výsledky předchozího vyhledávání.
1. Vyberte každou společnost, které chcete vydat produkty.
1. Vyberte **OK** pro zavření dialogového okna **Vydání** a návrat do pracovní plochy.
1. V podokně akcí na kartě **Změnový příkaz** ve skupině **Vydání produktu** vyberte **Proces** k vydání dotčených produktů vybraným společnostem. Případně vyberte **Uvolnit strukturu produktu** k zahájení procesu vydání.

## <a name="complete-the-change-order"></a>Dokončení změnového příkazu

Chcete-li označit změnový příkaz jako dokončený, což znamená, že nezbývají žádné další akce, vyberte možnost **Dokončit** v podokně akcí.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
