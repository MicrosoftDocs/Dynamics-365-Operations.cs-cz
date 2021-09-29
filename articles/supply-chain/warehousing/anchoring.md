---
title: Ukotvení
description: Toto téma vysvětluje, jak povolit a používat ukotvení.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505553"
---
# <a name="anchoring"></a>Ukotvení

[!include [banner](../includes/banner.md)]

Toto téma obsahuje podrobnosti o procesu ukotvení. Popisuje požadovanou konfiguraci a logiku, která je spuštěna, když pracovník skladu změní přechodné skladové místo nebo místo nakládky.

Funkce ukotvení vám umožňuje přepsat přechodné skladové místo nebo místo nakládky. Všechna otevřená vložení budou poté přesměrována na nové zadané přechodné skladové místo nebo místo nakládky.

Tato funkce může pomoci pracovníkům být efektivnější při odesílání zboží. Několik příkladů:

- Zaměstnanec, který musí vložit zboží v rámci objednávky 1 do přechodného skladového místa v překladišti 1, nemůže tuto operaci dokončit, protože předchozí náklad zatím neopustil skladové místo. Pracovník se rozhodne namísto čekání na uvolnění přechodného skladového místa překladiště 1 použít přechodné skladové místo překladiště 2. Proto pracovník přepíše navrhované přechodné skladové místo. Skladové místo pro všechny zbývající položky v rámci práce se poté aktualizuje na přechodné skladové místo 2. překladiště.
- Pracovník, který musí provést více výběrů pro stejnou dodávku, si může být jistý, že všechny vložené položky jsou sestaveny na stejném místě. Naložení položek do nákladního vozu proto vyžaduje méně času.

Ukotvení pro položky nabídky mobilního zařízení konfigurujete pomocí možnosti **Ukotvit**. Když tuto možnost nastavíte na *Ano*, můžete v poli **Ukotvit podle** určit, zda si přejete ukotvit podle dodávky nebo nákladu. Pokud nastavíte pole **Ukotvit podle** na *Dodávka*, následná otevřená vložení budou změněna na nové umístění dané zásilky. Pokud pole nastavíte na *Náklad*, následná otevřená vložení budou změněna na nové umístění pro tento náklad.

> [!IMPORTANT]
> Umístění pro následná otevřená vložení se změní pouze na pracovních řádcích, které jsou generovány ze stejného řádku pracovní šablony. Jinými slovy, systém ukotví řádky vložení, které pocházejí ze stejného řádku pracovní šablony.

Toto téma poskytuje scénář, který ukazuje, jak funguje ukotvení. Během scénáře vytvoříte sadu prodejních objednávek a uvolníte ji do skladu. Poté přepíšete navrhované přechodné skladové místo a ověříte, že veškerá zbývající práce při vyskladnění je směrována do nového umístění.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Předpoklad scénáře: Zpřístupnit ukázková data

Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na *USMF*, než začnete.

## <a name="scenario-setup"></a>Nastavení scénáře

Před zpracováním ukázkového scénáře musíte povolit ukotvení pro příslušnou položku nabídky mobilního zařízení.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Nastavení položky nabídky na mobilním zařízení pro povolení ukotvení

Chcete-li povolit ukotvení v položce nabídky mobilního zařízení, postupujte takto.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně seznamu vyberte záznam s názvem *Prodejní výdej*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte nebo nastavte pro záznam následující hodnoty:

    - **Název položky nabídky:** *Prodejní výdej*
    - **Nadpis:** *Prodejní výdej*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*
    - **Řídí:** *Řízeno uživatelem*
    - **Ukotvení:** *Ano*

        Toto nastavení způsobí, že systém během vyskladnění prodejů ukotví více řádků pracovní objednávky dohromady.

    - **Ukotvit podle:** *Náklad*

        Toto nastavení způsobí, že systém ukotví podle nákladu.

    - **Přepsat cílovou registrační značku vozidla:** *Ano*
    - **Přepsat registrační značku během vložení:** *Ano*
    - **Ponechat práci uzamčenou uživatelem:** *Ano*
    - **Povolit nadměrné vyskladnění:** *Ano*

### <a name="set-up-a-work-template-to-enable-staging"></a>Nastavení pracovní šablony pro povolení fázování

Chcete-li povolit fázování, konfigurujte pracovní šablonu podle těchto kroků. Tato konfigurace bude podporovat scénář, kdy pracovník umístí položky pro objednávku na přechodné skladové místo.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.
1. V mřížce vyberte pracovní šablonu **Fáze 61 PO**.
1. V části **Podrobnosti pracovní šablony** se ujistěte, že následující řádky existují a jsou konfigurovány podle zdejšího obrázku:

    - Řádek 1:

        - **Typ práce:** *Výdej*
        - **Povinné:** Vybráno (= *Ano*)
        - **ID pracovní třídy:** *Výdej PO*

    - Řádek 2:

        - **Typ práce:** *Vložit*
        - **Povinné:** Vybráno (= *Ano*)
        - **Kód předpisu:** *Fáze*
        - **ID pracovní třídy:** *Výdej PO*

    - Řádek 3:

        - **Typ práce:** *Výdej*
        - **Povinné:** Vybráno (= *Ano*)
        - **Zastavit práci:** *Ano*
        - **ID pracovní třídy:** *Nakládka PO*

    - Řádek 4:

        - **Typ práce:** *Vložit*
        - **Povinné:** Vybráno (= *Ano*)
        - **Kód předpisu:** *Portál*
        - **ID pracovní třídy:** *Nakládka PO*

1. V podokně akcí zvolte **Upravit dotaz** a otevřete editor dotazů.
1. Ujistěte se, že na kartě **Oblast** je přítomen následující řádek:

    - **Tabulka:** *Dočasné pracovní transakce*
    - **Odvozená tabulka:** *Dočasné pracovní transakce*
    - **Pole:** *Sklad*
    - **Kritéria:** *61*

1. Ujistěte se, že na kartě **Třídění** je přítomen následující řádek:

    - **Tabulka:** *Dočasné pracovní transakce*
    - **Odvozená tabulka:** *Dočasné pracovní transakce*
    - **Pole:** *ID dodávky*
    - **Směr hledání:** *Vzestupně*

1. Výběrem **OK** použijete nastavení a zavřete editor dotazů. Pokud se zobrazí výzva, přijměte změny.
1. V podokně akcí vyberte **Zalomení pracovních hlaviček**.
1. Na řádku, kde je pole **Název pole** nastaveno na *ID dodávky*, zkontrolujte, že je zaškrtnuto políčko **Seskupit podle tohoto pole**.

### <a name="set-up-license-plates-locations-and-inventory"></a>Nastavení registračních značek, umístění a zásob

Než vytvoříte prodejní objednávky a zásilky, musíte zajistit, aby existovala požadovaná umístění, registrační značky a zásoby.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Registrační značky** a vytvořte dvě registrační značky:

    - MyLP1
    - MyLP2

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění** a vytvořte následující umístění, pokud ještě nejsou k dispozici.

    | Sklad | Skladové místo   | ID profilu skladového místa | ID zóny   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | FLOOR     |
    | 61        | 06A01R3S1B | PICK-06             | FLOOR     |
    | 61        | STAGE01    | FÁZE               | *(Prázdné)* |
    | 61        | STAGE02    | FÁZE               | *(Prázdné)* |
    | 61        | STAGE03    | FÁZE               | *(Prázdné)* |
    | 61        | STAGE04    | FÁZE               | *(Prázdné)* |

1. Ujistěte se, že jsou k dispozici následující zásoby. Pokud musíte upravit zásoby, můžete vytvořit ruční pohyby, použít doplnění nebo využít jakýkoli jiný tok.

    | Č. položky | Množství | Sklad | Skladové místo   | Registrační značka |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Vytvoření poptávky

Předtím, než bude možné funkci ukotvení vyzkoušet, musíte vytvořit určitou poptávku. V tomto scénáři vytvoříte tři prodejní objednávky pro stejného zákazníka.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Výběrem možnosti **Nová** vytvořte první prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *61*

1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**. Pro tento řádek nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *1*

1. Na panelu nástrojů vyberte položku **Přidat řádek**, chcete-li přidat druhý řádek prodejní objednávky, a nastavte pro ni následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *1*

1. Opakujte následující kroky pro každý řádek prodeje v objednávce, abyste pro ně vyhradili zásoby:

    1. Na pevné záložce **Řádky prodejní objednávky** vyberte řádek prodejní objednávky.
    1. Na panelu nástrojů vyberte **Zásoby \> Rezervace**.
    1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži** a zavřete stránku.
    1. V podokně akcí vyberte **Uložit**.

1. Zopakováním kroků 2 až 6 vytvořte druhou prodejní objednávku. Pro tento řádek nastavte následující hodnoty:

    - V dialogu **Vytvořit prodejní objednávku**:

        - **Účet zákazníka:** *US-001*
        - **Sklad:** *61*

    - Na řádku prodejní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *2*

    - Na řádku prodejní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *2*

1. Opakujte krok 7 a rezervujte každý řádek v prodejní objednávce 2.
1. Zopakováním kroků 2 až 6 vytvořte třetí prodejní objednávku. Pro tento řádek nastavte následující hodnoty:

    - V dialogu **Vytvořit prodejní objednávku**:

        - **Účet zákazníka:** *US-001*
        - **Sklad:** *61*

    - Na řádku prodejní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *3*

    - Na řádku prodejní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *3*

1. Opakujte krok 7 a rezervujte každý řádek v prodejní objednávce 3.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Pomocí pracovní plochy plánování nákladu můžete vytvářet náklad a uvolňovat ho do skladu

Chcete-li vytvořit náklad pro objednávky, které jste vytvořili pro tento scénář, a poté ho uvolnit do skladu, postupujte takto.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. Na kartě **Řádky prodeje** najděte a vyberte všechny řádky prodejní objednávky pro prodejní objednávku 1 a prodejní objednávku 2.
1. V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**.
1. V dialogovém okně **Přiřazení šablony nákladu** v poli **ID šablony nákladu** vyberte šablonu nákladu, například *Standardní šablona nákladu*.
1. Zvolte **OK** a zavřete dialogové okno.
1. V části **Náklady** vyhledejte a vyberte náklad, který jste vytvořili.
1. V panelu nástrojů vyberte **Uvolnit \> Uvolnit do skladu**.
1. V dialogovém okně **Uvolnit náklad do skladu** výběrem **OK** uvolněte vybraný náklad do skladu.
1. Přejděte na **Řízení skladu \> Práce \> Všechna práce** k zobrazení práce, která byla vytvořena. Měli byste najít dvě nová pracovní ID, jedno pro každou zásilku. Každé ID práce má řádky výdeje a vkládání, které přenášejí zásoby z výdejních míst na přechodné skladové místo a z přechodného skladového místa do nákladové brány. Poznamenejte si hodnotu **ID práce** pro první dodávku, protože ji budete potřebovat v dalším postupu.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Výdej prodejní objednávky na přechodné skladové místo u první zásilky

1. Přihlaste se do mobilní aplikace Warehouse Management jako pracovník skladu *61*. (Ve standardních ukázkových datech se můžete přihlásit pomocí ID uživatele _61_ a hesla _1_.)
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Prodejní výdej**.
1. Vyberte pole **ID** a zadejte ID práce pro první zásilku.
1. Potvrďte zadání.
1. V poli **RZ** zadejte číslo registrační značky pro první položku (*MyLP1*).
1. Potvrďte zadání.
1. V poli **Cílová RZ** zadejte libovolné číslo (cílová registrační značka ještě nemusí existovat).

    Vyberete všechny řádky, které byly vytvořeny ze zpracované vlny, do stejné cílové poznávací značky.

1. Potvrďte zadání.
1. V poli **RZ** zadejte číslo registrační značky pro druhou položku (*MyLP2*).
1. Potvrďte zadání.

    Představte si, že pracovník nyní shromáždil objednávku, ale když se položky dostanou na přechodné skladové místo určené v práci, zjistí, že prostor je již obsazen. Pracovník však vidí, že je k dispozici jiné blízké místo (*STAGE03*). Proto požádá o změnu přechodného skladového místa. Protože je povolena funkce ukotvení, systém poté automaticky aktualizuje přechodné pracovní místo pro tuto a veškerou související práci.

1. Výběrem položky **Přepsat umístění** přepíšete navrhované přechodné skladové místo.
1. V poli **Výjimky práce** zadejte *Přechodný pruh se změnil*.
1. V poli **Umístění** zadejte nové přechodné skladové místo (*STAGE03*).
1. Potvrďte zadání. Zobrazí se zpráva „Práce dokončena“.
1. Přejděte do **Řízení skladu \> Práce\> Všechny práce**.
1. Otevřete ID práce pro první zásilku. Ověřte, že přechodné skladové místo bylo aktualizováno na nové umístění (*STAGE03*), které bylo definováno pomocí mobilního zařízení.
1. Otevřete ID práce pro druhou zásilku. Ověřte, že přechodné skladové místo bylo aktualizováno na nové přechodné skladové místo (*STAGE03*) z důvodu nastavení ukotvení.

> [!NOTE]
> Umístění všech zbývajících otevřených řádků práce vložení, které mají stejné přechodné skladové místo a které byly generovány ze stejného řádku pracovní šablony, bude aktualizováno na nové umístění.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Pomocí pracovní plochy plánování nákladu přidejte novou prodejní objednávku do stávajícího nákladu

Chcete-li do nákladu přidat objednávku a poté ji uvolnit do skladu, postupujte takto.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. Na kartě **Řádky prodeje** najděte a vyberte všechny řádky prodejní objednávky pro prodejní objednávku 3.
1. V podokně akcí na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do existujícího nákladu** a přidejte vybrané řádky objednávky do existujícího nákladu.
1. Zvolte **OK** a zavřete dialogové okno.
1. V části **Náklady** vyhledejte a vyberte náklad z předchozích kroků.
1. Vyberte **Uvolnění \> Uvolnění do skladu**.
1. V dialogovém okně **Uvolnit náklad do skladu** výběrem **OK** uvolněte vybraný náklad do skladu.
1. Přejděte na **Řízení skladu \> Práce \> Všechna práce** k zobrazení práce, která byla vytvořena. Poznamenejte si hodnotu **ID práce**, protože ji budete potřebovat v dalším postupu.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Výdej prodejní objednávky na přechodné skladové místo u třetí zásilky

1. Přihlaste se do mobilní aplikace jako pracovník ve skladu *61*.
1. V hlavní nabídce vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Prodejní výdej**.
1. Vyberte pole **ID** a zadejte ID práce pro třetí zásilku.
1. Potvrďte zadání.
1. V poli **RZ** zadejte číslo registrační značky pro první položku (*MyLP1*).
1. Potvrďte zadání.
1. V poli **Cílová RZ** zadejte libovolné číslo (cílová registrační značka ještě nemusí existovat).
1. Potvrďte zadání.
1. V poli **RZ** zadejte číslo registrační značky pro druhou položku (*MyLP2*).
1. Potvrďte zadání.

    Obdobně jako u prvního nákladu si představte, že pracovník zjistí, že zadané přechodné skladové místo není k dispozici. Proto chce použít jiné přechodné skladové místo (*STAGE04*).

1. Výběrem položky **Přepsat umístění** přepíšete navrhované přechodné skladové místo.
1. V poli **Výjimky práce** zadejte *Přechodný pruh se změnil*.
1. V poli **Umístění** zadejte nové přechodné skladové místo (*STAGE04*).
1. Potvrďte zadání. Zobrazí se zpráva „Práce dokončena“.
1. Přejděte do **Řízení skladu \> Práce\> Všechny práce**.
1. Otevřete ID práce pro první zásilku. Ověřte, že přechodné skladové místo nebylo aktualizováno na nové přechodné skladové místo (*STAGE04*), protože zbývající otevřený řádek vložení neodpovídá řádku pracovní šablony dokončeného řádku vložení.
1. Otevřete ID práce pro druhou zásilku. Ověřte, že přechodné skladové místo nebylo aktualizováno na nové přechodné skladové místo (*STAGE04*), protože přechodné skladové místo neodpovídá přechodnému skladovému místu dokončeného řádku vložení. Jinými slovy, dokončený řádek práce vložení a zbývající otevřený řádek práce mají různá přechodná skladová místa a v tomto případě se aktualizují pouze řádky, které mají stejná přechodná skladová místa.
1. Otevřete ID práce pro třetí zásilku. Ověřte, že přechodné skladové místo bylo aktualizováno na nové přechodné skladové místo (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
