---
title: "Přehled doručení"
description: "Toto téma obsahuje informace o funkci Přehled doručení. Stránka Přehled doručení je součástí této funkce a poskytuje přehled všech položek, které jsou očekávány jako příchozí položky."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9c174dc7bf61ffab0d20c7685a29007e0b6e2e7e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="arrival-overview"></a>Přehled doručení

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o funkci Přehled doručení. Stránka Přehled doručení je součástí této funkce a poskytuje přehled všech položek, které jsou očekávány jako příchozí položky.

Stránka **Přehled doručení** uvádí přehled všech očekávaných příchozích položek. Zobrazuje také doručení, která mohou být inicializována na základě přehledu. Toto téma se zaměřuje na proces příjmu.

## <a name="business-scenario"></a>Obchodní scénář
Předpokládejme následující scénář v příchozích procesech.

[![Obchodní scénář](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Marek, přijímající pracovník, chce vědět, co má být přijato na aktuální den. Na stránce **Přehled doručení** může Marek získat přehled aktuálních úkolů a hrubý odhad množství, objemu, hmotnosti, různých typů objednávek atd. Později je dodávka doručena do jednoho vstupního překladiště a Marek přijme přehled její přehled. Na stránce **Přehled doručení** může Marek provádět následující úlohy:

-   Identifikujte odpovídající příjem objednávky a zaregistrujte příjem jako **Probíhá**. Řádky, které jsou vyžadovány pro provedení registrace, jsou automaticky generovány a příjem lze sledovat, přestože transakce ještě nebyly zaúčtovány jako **Registrované**.
-   Přejděte na vhodnou deníkovou referenci doručení (tj. deník **Doručení zboží** nebo **Vstup výroby**) a určete deníky, které jsou připraveny na aktualizaci potvrzení produktu.

## <a name="arrival-overview-page"></a>Stránka Přehled doručení
Chcete-li otevřít stránku **Přehled doručení**, klikněte na možnost **Řízení zásob** &gt; **Příchozí objednávky** &gt; **Přehled doručení**. Můžete zobrazit seznam objednávek, které mají být přijaty. Přehled je rozdělen do záhlaví a řádků. Informace v záhlaví jsou seskupeny podle typu objednávky, očekávaného data převzetí a cíle dodávky. Když je vybraný řádek záhlaví pro doručení, všechny řádky podrobností, které se vztahují k odkazu příjemky, jsou vybrány pro doručení v části podrobností řádku na stránce. Po zaúčtování všech souvisejících řádků deníku souvisejících se tyto informace nezobrazí.

### <a name="arrival-overview-profiles"></a>Profily přehledu doručení

Stránka **Přehled doručení** uvádí přehled položek, u kterých se očekává doručení, a datum, kdy mají být doručeny. V rámci procesu doručení lze použít více sad osobních nastavení. Jednotliví uživatelé mohou definovat své vlastní nastavení na stránce **Profily přehledu doručení**.

### <a name="set-up-item-arrival"></a>Nastavení doručení zboží

V našem příkladu chce Marek nastavit nový počítač v místě, které bude použito k příjmu hotových výrobků, které pocházejí z výroby na pracovišti 1. Na stránce **Profily přehledu doručení** Marek vytvoří nové nastavení s názvem **Výroba na pracovišti 1** a určí následující nastavení.

1.  Na pevné záložce **Možnosti doručení** ve skupině polí **Rozsah** skupiny zadejte informace o denním intervalu a skladech, které chcete zahrnout do přehledu.
2.  Na pevné záložce **Možnosti doručení** ve skupině polí **Deník** zadejte přijímací sklad, umístění a název deníku (doručení položky/vstup do výroby).
3.  Na pevné záložce **Podrobnosti dotazu na doručení** ve skupině polí **Pracoviště** v poli **Omezit na pracoviště** zadejte pracoviště pro omezení zobrazení v oblasti přehled.
4.  Na pevné záložce **Podrobnosti o dotazu na doručení** ve skupině polí **Zobrazené typy transakcí**, nastavte možnost **Výrobní zakázky** na **Ano**.
5.  Na pevné záložce **Podrobnosti o dotazu na doručení** ve skupině **Různé** skupiny, nastavte možnost **Aktualizovat při spuštění** na **Ano**, pokud má při spuštění být automaticky aktualizováno zobrazení. Nastavte možnost **Aktualizovat při změně rozsahu** na **Ano**, pokud má být zobrazení automaticky aktualizováno při změně hodnot rozsahu.

V tomto příkladu je hodnota v poli **Název profilu přehledu doručení** na pevné záložce **Možnosti doručení** stránky **Přehled doručení** nastavena na **Výrobní pracoviště 1**.

### <a name="prerequisites-for-arrival-journals"></a>Předpoklady pro deníky doručení

Pro automatické vytváření deníků doručení ze stránky **Přehled doručení** je nutné definovat příslušné informace ve skupině polí **Deník** na pevné záložce **Možnosti doručení**.

-   Při vytváření nového deníku je nutné zadat název deníku.

[![Zadání názvu deníku](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Pokud zadáte hodnoty do polí **Sklad** a **Umístění**, použijí se tyto hodnoty na řádcích deníku. Pokud hodnoty nezadáte, systém použije hodnoty z dimenze, která je určena ve skladových transakcích.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Položky, které byly přijaty z jednoho očekávaného příjmového dokladu

Na pevné záložce **Příjmy** Marek vybere řádek a klikne na **Zahájit doručení**. Automaticky jsou vybrány všechny související řádky, které jsou v určeném rozsahu a které mají množství k registraci. Je generován deník doručení položek, který obsahuje shodu mezi očekávaným příjmovým dokladem a deníkem. Množství se inicializuje automaticky na všech řádcích, které jsou vytvořeny.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Položky, které byly přijaty z více než jednoho očekávaného příjmového dokladu

Na pevné záložce **Příjmy** Marek vybere více řádků a klikne na **Zahájit doručení**. Je generován deník doručení položek, který obsahuje shodu mezi všemi očekávanými objednávkami doručení a deníkem. Všechny řádky jsou vytvořeny v jednom záhlaví deníku doručení položky a množství se inicializuje automaticky.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Příjem položek z jedné nebo více očekávaných objednávek příjmu

#### <a name="view-information"></a>Zobrazit informace

Pro získání přehledu očekávaných příjmů v datovém intervalu Marek zadá následující informace do polí na pevné záložce **Možnosti doručení** na stránce **Přehled doručení** a potom klikne na tlačítko **Aktualizovat** pro aktualizaci zobrazení:

-   Název profilu přehledu doručení: **Dotaz**
-   Zobrazit řádky: **Všechny**
-   Dny zpětně. (Prázdné)
-   Dny dopředu: **0**
-   Sklady: **GW, MW**

Marek může zobrazit následující informace:

-   Všechny související příjmové doklady do systémového data a nekonečný počet dnů zpět od něj (interval **InventTrans.StatusDate**) a příjemky pro sklad GW a MW, bez ohledu na stav.
-   Podrobné informace o řádku pro více než jednu objednávku. Marek může vybrat několik řádků záhlaví přehledu a klepnutím na tlačítko **Zobrazit všechny vybrané** zobrazit všechny podrobné informace o odpovídajícím řádku pro všechny vybrané objednávky.
-   Informace o konkrétní nákupní objednávce. Aby se zobrazily pouze informace, které souvisí s určitým referenčním číslem v přehledu, může Marek zadat číslo účtu v poli **Číslo účtu** a číslo objednávky v poli **Referenční číslo**.
-   Přehled úkolů registrace, které mají být splněny pro všechny řádky objednávky, pro něž byl vytvořen deník doručení položky, ale dosud nebyly zaúčtovány. K zobrazení těchto informací může Marek vybrat možnost **Probíhá** v poli **Zobrazit řádky**.

### <a name="update-journals"></a>Aktualizace deníků

K registraci jednoho nebo více řádků objednávky, které mají být zpracovány může Marek vybrat řádky v mřížce přehledu nebo řádek a pak kliknout na **Deníky** &gt; **Zobrazit doručení z příjemek**. Zobrazí se záhlaví doručení položky, odpovídající řádkům. Pro účely aktualizace registrovaných položek na příjmu nákupní objednávky může Marek přejít do záhlaví deníku doručení zboží, které je připravené k aktualizaci. Pro přístup k těmto záhlavím klikne na **Deníky** &gt; **Deníky přípravy příjmu produktu**. Zobrazí se všechny řádky záhlaví, které jsou připraveny na aktualizaci příjemky produktu v zadaném rozsahu skladu. (Zobrazené řádky záhlaví nesouvisejí s intervalem dne).

### <a name="start-an-arrival-registration"></a>Zahájení registrace doručení

Výběrem více řádků na stránce **Přehled doručení** může Marek zahájit doručení více než jedné reference příjemky. Když vybere řádek z přehledu příjmů, budou vybrány podrobnosti o příslušném řádku. Existuje-li množství k registraci, bude k dispozici tlačítko **Zahájit doručení**. Marek může zahájit registraci doručení dvěma způsoby:

-   Může nastavit filtrování stránky tak, aby se zobrazily pouze záznamy splňující specifická kritéria, v poli **Odkaz na dodavatele**, naskenovat referenční číslo od dodavatele, jako je například čárový kód pro dodací list.
-   V části Přehled nebo podrobnostech stránky **Přehled doručení** ručně vyberte nebo zrušte výběr záznamů pro registraci doručení. Když potom Marek klikne na tlačítko **Zahájit doručení**, v deníku doručení položky budou automaticky vytvořeny vybrané záznamy. Záznamy zahrnují informace o řádku a jsou přiřazeny informace o všech jednoznačných polích.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Aktualizace informací o doručení a zpracování příjemky produktu
Po zaregistrování veškerého zboží může vedoucí skladu nebo vedoucí nákupu aktualizovat přijaté položky údaji z příjemku produktu, čímž přidá fyzické náklady. Chcete-li aktualizovat informace o doručení a zaúčtovat příjemku produktu, postupujte následujícím způsobem.

1.  Klikněte na **Řízení zásob** &gt; **příchozí objednávky** &gt; **přehled doručení**.
2.  Na stránce **Přehled doručení** klepněte na **Deníky** &gt; **Deníky připravené na příjemky produktů** pro zobrazení seznamu deníků, které jsou připraveny na aktualizaci příjemky produktu.
3.  Vyberte deníky, které je třeba aktualizovat, a klikněte na **Funkce** &gt; **Příjemky produktu**.
4.  Na stránce **Zaúčtování** zadejte číslo příjemky produktu, pokud již není k dispozici v deníku, a klikněte na tlačítko **OK** pro zpracování příjemky produktu.

## <a name="summary"></a>Souhrn
Stránka **Přehled doručení** může pomoci vedoucímu skladu a pracovníkům skladu dosáhnout přehledu očekávaných prací, které je třeba provést jako součást příchozího procesu. Na této stránce můžete také spustit proces doručení položky k zajištění, že položky budou sledovány v první položce skladu.

