---
title: Expedice malých balíků
description: Toto téma obsahuje informace o funkci expedice malých balíků (SPS). Tato funkce umožňuje produktu Microsoft Dynamics 365 Supply Chain Management odeslat přepravci podrobnosti o zabaleném kontejneru a poté od něj obdržet přepravní štítek, sazbu za dopravu a sledovací číslo.
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 350193a0054ef879ece3dd2dfcc4105476981837
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078241"
---
# <a name="small-parcel-shipping"></a>Expedice malých balíků

[!include [banner](../includes/banner.md)]

Funkce přepravy malých balíčků (SPS) umožňuje produktu Microsoft Dynamics 365 Supply Chain Management přímo komunikovat s přepravci poskytnutím rámce pro komunikaci prostřednictvím API dopravce. Tato funkce je užitečná, když odesíláte jednotlivé prodejní objednávky prostřednictvím komerčních přepravců místo použití kontejnerové přepravy nebo přepravy méně než nákladní vůz (LTL).

Funkce SPS interaguje s vaším dopravcem prostřednictvím vyhrazeného *výpočtu přepravních sazeb*. Vaše organizace musí tento výpočet přepravních sazeb vyvinout ve spolupráci s vaším dopravcem nebo službou dopravního centra. Výpočet přepravních sazeb umožňuje produktu Supply Chain Management odeslat přepravci podrobnosti o zabaleném kontejneru a poté od něj obdržet přepravní štítek, sazbu za dopravu a sledovací číslo.

Vrácená sazba za přepravu se přidá k související prodejní objednávce jako různé poplatky. Vrácený přepravní štítek lze poté automaticky vytisknout pomocí tiskárny ZPL (Zebra Programming Language) a použít na zásilku. Přepravce tento přepravní štítek naskenuje, když vyzvedne balíčky ve skladu.

## <a name="prepare-your-system-to-support-sps"></a>Příprava systému na podporu SPS

Než budete moci začít používat funkce SPS, musíte zapnout funkci SPS ve Správě funkcí, přidat modul rychlosti a nastavit moduly **Řízení dopravy** a **Vedení skladu** na jeho podporu.

### <a name="turn-on-the-sps-feature"></a>Zapnutí funkce SPS

Než můžete použít funkci SPS, musíte ji zapnout ve svém systému. Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Správa přepravy*
- **Název funkce:** *Expedice malých balíků*

### <a name="deploy-and-set-up-rate-engines"></a>Nasazení a nastavení výpočtu přepravních sazeb

Supply Chain Management nezahrnuje žádné výpočty přepravních sazeb. Musíte získat nebo vytvořit jakékoli výpočty přepravních sazeb, které požadujete, a poté je přidat do svého systému. Společnost Microsoft však poskytuje ukázkový výpočet přepravních sazeb, který můžete použít k testování.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Stažení a nasazení ukázkového výpočtu přepravních sazeb

Chcete-li získat ukázkový výpočet přepravních sazeb, postupujte podle těchto pokynů.

1. Na GitHubu si stáhněte [knihovnu DLL pro ukázkový výpočet přepravních sazeb](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Na serveru Supply Chain Management uložte knihovnu DLL do složky **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\zásobník**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Vytvoření a nasazení funkčních výpočtů přepravních sazeb

Informace o tom, jak vytvořit a nasadit funkční výpočty přepravních sazeb, aby je bylo možné použít v produkčním nebo testovacím prostředí, najdete v následujících tématech:

- [Vytvoření nového modulu správy přepravy](../transportation/create-new-transportation-management-engine.md)
- [Nastavení modulů správy přepravy](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Další informace o tom, jak vytvořit výpočet přepravních sazeb SPS, najdete v následujícím příspěvku na blogu: [Expedice malých balíků: Jak využít funkce expedice malých balíků v Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Nastavení výpočtu přepravních sazeb v Supply Chain Management

Poté, co jste vytvořili a nasadili výpočet přepravních sazeb pro SPS, nastavte jej podle těchto kroků.

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Moduly \> Výpočet přepravních sazeb**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující pole:

    - **Výpočet přepravních sazeb** - Zadejte jedinečný název pro výpočet přepravních sazeb. Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *ukázkový výpočet přepravních sazeb*.
    - **Název** - Zadejte stručný popis výpočtu přepravních sazeb. Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *ukázkový výpočet přepravních sazeb*.
    - **ID metadat hodnocení** - Vyberte základ, který by se měl použít k výpočtu vaší sazby. Například vaše sazba může být vypočítána na základě vzdálenosti. Pokud používáte ukázkový výpočet přepravních sazeb, můžete toto pole nechat prázdné.
    - **Sestava modulu** - Zadejte název souboru balíčku DLL, který jste nasadili. Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *TMSSmallParcelShippingEngine.dll*.
    - **Třída modulu** - Zadejte název třídy, který byl stanoven pro váš výpočet přepravních sazeb. Pokud používáte ukázkový výpočet přepravních sazeb, zadejte *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Příklad

Tento příklad scénáře ukazuje, jak nastavit a používat SPS poté, co jste připravili systém, jak je popsáno výše v tomto tématu. Tento scénář používá dříve zmíněný ukázkový výpočet přepravních sazeb.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

### <a name="set-up-the-scenario"></a>Nastavení scénáře

V tomto příkladu scénáře musíte mít ukázkového přepravce, skupinu přepravců, zásady balení a profil balení. Následující podsekce vysvětlují, jak připravit záznamy, které jsou pro scénář vyžadovány. V produkčním scénáři se proces instalace obvykle podobá procesu, který je zde popsán. Nastavíte však jiné hodnoty.

#### <a name="set-up-carriers"></a>Nastavení dopravců

Chcete-li nastavit dopravce, postupujte následujícím způsobem:

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Dopravci \> Dopravci dodávky**.
1. V podokně Akce vyberte možnost **Nový** a přidejte dopravce.
1. V záhlaví nastavte následující hodnoty:

    - **Dopravce dodávky:** *Demo Carrier*
    - **Jméno:** *Demo Carrier*
    - **Režim:** *Pozemní*

1. Na pevné záložce **Přehled** nastavte následující hodnoty:

    - **Aktivace rozhraní dopravců:** *Ano*
    - **Aktivace hodnocení dopravce:** *Ano*

1. Na záložce s náhledem **Služby** přidejte službu do mřížky výběrem možnosti **Nový**.
1. Nastavte následující hodnoty pro novou službu:

    - **Služba přepravce:** *Demo carrier service*
    - **Jméno:** *Demo Carrier service*
    - **Způsob přepravy:** *pozemní*

    Podle potřeby zadejte hodnoty pro všechna ostatní pole. (Když uložíte nový záznam přepravce, vytvoří se nový způsob doručení a pole **Způsob dodání** bude nastaveno automaticky.)

1. Na záložce s náhledem **Profily sazeb** vyberte **Nový** a vytvořte profil sazeb pro mřížku.
1. Nastavte následující hodnoty pro nový profil:

    - **Profil hodnocení:** *Ukázková služba dopravce*
    - **Jméno:** *Demo Carrier service*
    - **Výpočet přepravních sazeb:** *Ukázkový výpočet přepravních sazeb*

    Podle potřeby zadejte hodnoty pro všechna ostatní pole.

1. V podokně akcí vyberte **Uložit**.

Další informace o postupu při nastavení dopravců získáte v tématu [Nastavení dopravců](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Nastavení účtů služeb dopravce

Pokud chcete nastavit účet služby dopravce, postupujte následovně.

1. Přejděte do nabídky **Správa přepravy \> Nastavení \> Hodnocení \> Náklady na účet služeb dopravce**.
1. V podokně akcí vyberte možnost **Nový** pro přidání účtu služby dopravce.
1. Nastavte následující hodnoty pro nový účet:

    - **Dopravce:** *Ukázkový dopravce*
    - **Služba přepravce:** *Demo carrier service*
    - **Číslo účtu dopravce:** Číslo účtu zákazníka dopravce, které se používá k ověření a potvrzení připojení k dopravci. Tuto hodnotu poskytne váš dopravce. Pokud používáte ukázkovou službu, můžete zadat libovolnou hodnotu.
    - **Lokalita:** *6*
    - **Sklad:** *62*

    > [!NOTE]
    > Často je hodnota **Číslo zákaznického účtu dopravce** jediná hodnota, která je vyžadována k ověření připojení. Pokud však váš operátor vyžaduje další parametry ověřování, měla by vaše organizace přizpůsobit tuto stránku a podle potřeby přidat další pole.

#### <a name="set-up-a-container-packing-policy"></a>Nastavení zásad balení kontejneru

Pokud chcete nastavit zásady balení kontejneru, postupujte následovně.

1. Pokud jste ještě nenastavili definici tiskárny ZPL, použijte ji k nastavení aplikace Document Routing Agent. Další informace viz [Přehled tisku dokumentů](../../fin-ops-core/dev-itpro/analytics/print-documents.md) a související témata.
1. Přejděte na **Řízení skladu \> Nastavení \> Kontejnery \> Zásady balení kontejneru**.
1. V podokně akcí vyberte možnost **Nový** pro přidání zásad balení kontejneru.
1. V záhlaví nové zásady nastavte následující hodnoty:

    - **Zásady balení kontejnerů:** *Ukázka zásad balení*
    - **Popis:** Popis zásad

1. Na pevné záložce **Přehled** nastavte následující hodnoty:

    - **Sklad:** *62*
    - **Výchozí umístění pro konečnou zásilku:** *Baydoor*
    - **Jednotka hmotnosti:** *KG*
    - **Zásady uzavírání kontejnerů:** *Automatické vydání*
    - **Zásady pro uvolňování kontejnerů:** *Zpřístupnit na konečném místě dodání*

1. Na záložce s náhledem **Obecné** můžete nastavit následující hodnoty:

    - **Automatický manifest při zavření kontejneru:** *Ano*
    - **Požadavky manifestu pro kontejner:** *Správa dopravy*
    - **Obsah tiskového kontejneru:** *Ne*

1. Na záložce s náhledem **Tisk štítku dopravce** můžete nastavit následující hodnoty:

    - **Vytisknout přepravní štítek kontejneru:** *Vždy*
    - **Název tiskárny:** Název tiskárny ZPL, která by měla tisknout přepravní štítky

#### <a name="set-up-a-packing-profile"></a>Nastavení profilu balení

Chcete-li nastavit profil balení, postupujte následujícím způsobem:

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Balení \> Profily balení**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá profil balení do mřížky.
1. Nastavte následující hodnoty pro nový profil:

    - **ID profilu balení:** *Ukázka profilu balení*
    - **Popis:** Popis profilu
    - **Zásady balení kontejnerů:** *Ukázka zásad balení*
    - **Režim ID kontejneru:** *Automatický*
    - **Typ kontejneru:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Nastavení zákazníka, aby používal dopravce SPS

Pomocí těchto kroků nastavíte zákazníka tak, aby mohl používat vámi vytvořeného operátora.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. V mřížce vyhledejte a vyberte odběratele *US-027*.
1. V podokně akcí na kartě **Obecné** ve skupině **Nastavení** zvolte **Účty odběratele dopravce**.
1. Na stránce **Účty zákazníků dopravce**, v podokně akcí vyberte **Nový** pro přidání účtu do mřížky.
1. Nastavte následující hodnoty pro nový účet:

    - **Dopravce dodávky:** *Demo Carrier*
    - **Číslo účtu přepravce:** *12345* (Hodnota není pro tento scénář důležitá, ale bude na ni odkazováno v další části.)

### <a name="go-through-the-example-scenario"></a>Projděte si ukázkový scénář

Poté, co nastavíte všechna ukázková data, jak je popsáno v předchozí části, jste připraveni projít ukázkovým scénářem.

#### <a name="create-a-sales-order-and-process-the-work"></a>Vytvoření prodejní objednávky a zpracování práce

Chcete-li vytvořit prodejní objednávku, postupujte následujícím způsobem.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvořit prodejní objednávku** nastavte v poli **Účet odběratele** hodnotu *US-027*.
1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Na kartě s náhledem **Záhlaví prodejní objednávky** nastavte hodnotu v poli **Číslo účtu odběratele dopravce** na hodnotu, kterou jste pro tohoto odběratele vybrali předtím (*12345*).
1. V části **Řádky prodejní objednávky** přidejte řádek prodeje a nastavte pro něj následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *1*
    - **Lokalita:** *6*
    - **Sklad:** *62*

1. Přepněte na zobrazení **Záhlaví**.
1. Na záložce s náhledem **Doručení** nastavte následující hodnoty:

    - **Dopravce dodávky:** *Demo Carrier*
    - **Služba přepravce:** *Demo carrier service*

1. Přepněte znovu do zobrazení **Řádky**. Pokud se zobrazí výzva k aktualizaci způsobu doručení prodejních linek, vyberte **Ano**.
1. V části **Řádky prodejní objednávky** vyberte řádek objednávky, který jste nastavili dříve, a poté vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Je vytvořeno dílo pro přesun položek z místa vychystávání do balicí stanice.

1. V části **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti o dodávce**.
1. Na stránce **Podrobnosti o zásilce** si poznamenejte ID dodávky. Budete ho potřebovat, až zabalíte dodávku na balicí stanici.
1. Zavřete stránku **Podrobnosti o dodávce** a vraťte se k prodejní objednávce.
1. Poznamenejte si číslo prodejní objednávky a přejděte na **Řízení skladu \> Práce \> Všechny práce**.
1. Pomocí čísla prodejní objednávky vyhledejte a vyberte práci, která byla pro objednávku vytvořena.
1. V podokně akcí na kartě **Práce** zvolte **Dokončit práci**.
1. Na stránce **Dokončení práce** v poli **ID uživatele** vyberte ID uživatele. Pak v podokně akcí vyberte možnost **Ověřit práci**.
1. Pokud práce projede ověřením, vyberte **Dokončit práci** v podokně akcí.

    Práce je označena jako dokončená pro simulaci pohybu věcí do balírny.

#### <a name="pack-the-shipment"></a>Zabalení dodávky

Chcete-li zpracovat dodávku, postupujte následovně.

1. Jděte na **Řízení skladu \> Nastavení \> Pracovník** a ujistěte se, že je váš uživatelský účet přidružen k pracovnímu účtu pro správu skladu.
1. Přejděte na **Řízení skladu \> Vyzvednutí a kontejnerizace \> Balení**.
1. V dialogovém okně **Vybrat balicí stanici** nastavte následující hodnoty:

    - **Lokalita:** *6*
    - **Sklad:** *62*
    - **Místo:** *balení*
    - **ID profilu balení:** *Ukázka profilu balení*

1. Vyberte **OK**.
1. Zobrazí se stránka **Balení**. V produkčním scénáři pracovník naskenuje registrační značku nebo ID zásilky. U tohoto scénáře však otevřete stránku **Všechny zásilky** a vyhledejte číslo zásilky, kterou jste právě vytvořili. Poté zadejte tuto hodnotu do pole **Registrační značka nebo zásilka** na straně **Balíček**. Případně zadejte ID zásilky, které jste si dříve poznamenali.
1. V podokně akcí zvolte **Nový kontejner**.
1. Zobrazí se dialogové okno, které zobrazuje podrobnosti o novém kontejneru. Nechejte výchozí hodnoty a poté vyberte **OK**.
1. Na stránce **Balení** na kartě s náhledem **Balení zboží** v poli **Identifikátor** vyberte *A0002* pro zabalení této položky. Položka je přidána do kontejneru.
1. V podokně akcí klikněte na možnost **Kontejnery pro dodávku**.

    Stránka **Kontejnery pro dodávku**, která se zobrazí, má řádek pro kontejner, který jste právě vytvořili. Pole **ID manifestu kontejneru** v tomto řádku je však aktuálně prázdné, protože jste od dopravce dosud neobdrželi přepravní štítek a sledovací číslo.

1. V podokně akcí zvolte **Zavřít kontejner**.
1. V dialogovém okně **Zavřít kontejner** nastavte pole **Hrubá hmotnost** na *1 kg* a potom vyberte **OK**.

    Přepravní štítek by nyní měl být vytištěn na tiskárně ZPL, kterou jste vybrali dříve. Výsledek by měl vypadat podobně jako v následujícím příkladu.

    ![Příklad expedičního štítku](media/sps-label-example.png "Příklad expedičního štítku")

1. Všimněte si, že hodnoty **ID manifestu kontejneru** a **Celkem dopravné** byly přidány jako přijaté od dopravce.
