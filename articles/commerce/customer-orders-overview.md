---
title: Objednávky zákazníků v pokladním místě (POS)
description: Toto téma obsahuje informace o objednávkách zákazníků v pokladním místě (POS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuzi o souvisejících parametrech a transakčních tocích.
author: josaw1
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 44beb4515bf0d2f8fc7ad75feb3164bf1c7c2d5737552b1a06ce59c2edcaf8fe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755076"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Objednávky zákazníků v pokladním místě (POS)

[!include [banner](includes/banner.md)]

Toto téma obsahuje informace, jak vytvořit a spravovat objednávky zákazníků v aplikaci Pokladním místo (POS). Objednávky zákazníků lze použít k zaznamenání prodejů, kdy si odběratelé chtějí vyzvednout produkty později, vyzvednout si produkty z jiného místa nebo si nechat zboží odeslat. 

Ve světě omni-channel commerce celá řada maloobchodních prodejců poskytuje možnost objednávek odběratele neboli speciálních objednávek, aby splnili různé požadavky týkající se produktu a plnění. Zde jsou některé typické scénáře:

- Zákazník chce, aby produkty byly doručeny k určitému datu na konkrétní adresu.
- Zákazník chce vyzvednout výrobky ve skladu nebo z místa, které se liší od skladu nebo místa, kde zákazník tyto produkty zakoupil.
- Zákazník si přímo v obchodě dnes objedná produkty a později si je chce vyzvednout ve stejném obchodě.

Maloobchodní prodejci mohou používat objednávky zákazníků pro minimalizaci ztrát prodeje, které by jinak výpadky zásob mohly způsobit, protože zboží lze doručit nebo vyzvednout v jiném čase nebo na jiném místě.

## <a name="set-up-customer-orders"></a>Nastavení objednávek odběratele
Než vyzkoušíte funkci objednávek zákazníků v POS, nezapomeňte provést všechny potřebné konfigurace v centrále Commerce.

### <a name="configure-modes-of-delivery"></a>Konfigurace způsobů dodání

Chcete-li používat objednávky zákazníků, musíte nakonfigurovat způsoby dodání, které může kanál obchodu používat. Musíte definovat alespoň jeden způsob dodání, který lze použít, když jsou řádky objednávky odeslány odběrateli z obchodu. Musíte také definovat alespoň jeden způsob vyskladnění dodávky, který lze použít, když jsou řádky objednávky vyzvednuty z obchodu. Způsoby doručení jsou definovány na stránce **Způsoby dodání** v centrále Commerce. Další informace o nastavení způsobů dodání pro kanály Commerce naleznete v tématu [Definování způsobů dodání](./configure-call-center-delivery.md#define-delivery-modes).

![Stránka Způsoby dodání.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Nastavení skupin plnění

Některé obchody nebo sklady nemusí být schopny plnit objednávky zákazníků. Konfigurací skupin plnění může organizace určit, která umístění obchodu a skladu se zobrazí jako možnosti uživatelům, kteří vytvářejí objednávky zákazníků v POS. Skupiny plnění jsou konfigurovány na stránce **Skupiny plnění**. Organizace mohou vytvořit tolik skupin plnění, kolik požadují. Poté, co je definována skupina plnění, propojte ji s obchodem výběrem možnost **Přiřazení skupiny plnění** na kartě **Nastavení** v podokně Akce na stránce **Obchody**.

V Commerce verze 10.0.12 a novějších mohou organizace definovat, zda lze sklad nebo kombinaci sklad a obchod, které jsou definovány ve skupinách plnění, použít k přepravě, k vyzvednutí nebo k přepravě a vyzvednutí. To umožňuje podnikům větší flexibilitu při určování, které sklady lze vybrat při vytváření objednávky zákazníka k odeslání zboží, a které obchody lze vybrat při vytváření objednávky zákazníka pro vyzvednutí zboží. Chcete-li využít výhod těchto možností konfigurace, zapněte funkci **Možnost specifikovat místa jako „Expedice“ nebo „Výdej“ povolena ve skupině plnění**. Pokud sklad, který je propojen se skupinou plnění, není obchod, lze jej nakonfigurovat pouze jako místo expedice. Nelze jej použít, když jsou objednávky pro výdej konfigurovány v POS.

![Stránka Skupiny plnění.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Konfigurace nastavení kanálu

Při práci s objednávkami zákazníků v POS musíte zvážit některá nastavení kanálu obchodu. Tato nastavení najdete na stránce **Obchody** v centrále Commerce.

- **Sklad** - Toto pole označuje sklad, který bude použit při snižování zásob pro objednávky cash and carry a vyzvednutí zákazníkem vázané na tento obchod. Jako osvědčený postup doporučujeme používání jedinečných skladů pro každý kanál obchodu, aby se zabránilo konfliktním problémům obchodní logiky napříč obchody.
- **Expediční sklad** - Toto pole označuje sklad, který bude použit při snižování zásob pro objednávky zákazníka, které budou expedovány z vybraného obchodu. Pokud je funkce **Možnost zadat umístění jako „Expedice“ nebo „Vyzvednutí“ povoleno ve skupině plnění** ve vašem prostředí povolena, mohou si uživatelé POS vybrat konkrétní sklad, ze kterého se bude odesílat v POS, místo aby si vybrali obchod, ze kterého se bude odesílat. Když je tedy tato funkce povolena, expediční sklad se již nevyužívá, protože uživatel si při vytvoření objednávky vybere konkrétní sklad, ze kterého bude expedována objednávka.
- **Přiřazení skupiny plnění** – Vyberte toto tlačítko (na kartě **Nastavení** v podokně Akce), chcete-li propojit odkazované skupiny plnění, aby se zobrazily možnosti míst výdeje nebo původů dodávky při vytváření objednávek zákazníků v POS.
- **Použít daň podle místa určení** – Tato možnost určuje, zda se dodací adresa použije k určení daňové skupiny, která se použije na řádky objednávky, které jsou dodávány na adresu zákazníka.
- **Použít daň podle zákazníka** – Tato možnost určuje, zda se daňová skupina, která je definována pro doručovací adresu zákazníka, použije k zdanění objednávek zákazníků, které jsou vytvořeny v POS pro odeslání k zákazníkovi domů.

![Nastavení kanálu obchodu na stránce Obchody.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Nastavení parametrů objednávek zákazníků

Než budete vytvářet objednávky zákazníků v POS, musíte nakonfigurovat příslušné parametry v centrále Commerce. Tyto parametry naleznete na kartě **Objednávky zákazníka** na stránce **Parametry Commerce**.

- **Výchozí typ objednávky** – Můžete určit typ objednávky, který je standardně přiřazen k objednávkám zákazníků, které jsou vytvořeny v POS. Tyto objednávky zákazníků mohou být buď prodejní objednávky nebo objednávky nabídek. Bez ohledu na výchozí typ objednávky mohou uživatelé i nadále vytvářet prodejní objednávky i objednávky zákazníků z POS.
- **Výchozí procento zálohy** – Zadejte procento celkové částky objednávky, kterou musí zákazník zaplatit jako zálohu před tím, než může objednávku potvrdit. V závislosti na svých oprávněních mohou zaměstnanci obchodu přepsat částku pomocí operace **Přepsání zálohy** v POS, pokud je tato operace nakonfigurována pro rozložení obrazovky transakce.
- **Způsob vyskladnění dodávky** – Určete způsob dodání, který by se měl použít na řádky prodejní objednávky, které jsou nakonfigurovány pro vyzvednutí v POS.
- **Způsob doručení/převzetí** – Určete způsob doručení, který by se měl použít na řádky prodejní objednávky, které se při vytvoření smíšeného košíku považují za řádky předávací objednávky, kde budou některé řádky vyzvednuty nebo odeslány a další řádky si zákazník odnese okamžitě.
- **Procento poplatku za zrušení** – Pokud má být použit poplatek při zrušení objednávky zákazníka, určete výši tohoto poplatku.
- **Kód poplatku za zrušení** – Určete kód poplatku za pohledávky, který by se měl použít, když je účtován storno poplatek za zrušené objednávky zákazníků prostřednictvím POS. Kód poplatku definuje logiku finančního účtování poplatku za zrušení.
- **Kód dopravného** – Pokud je možnost **Použít rozšířené automatické náklady** nastavena na **Ano**, toto nastavení parametrů nemá žádný účinek. Pokud je tato možnost nastavena na **Ne**, uživatelé budou při vytváření objednávek zákazníků v POS vyzváni k ručnímu zadání dopravného. Tento parametr použijte k mapování kódu poplatků za pohledávky, který se použije na objednávky, když uživatelé zadají dopravné. Kód poplatku definuje logiku finančního účtování dopravného.
- **Použít rozšířené automatické náklady** – Nastavte tuto možnost na **Ano**, chcete-li používat systémem počítané automatické poplatky, když jsou objednávky zákazníků vytvořeny v POS. Tyto automatické náklady lze použít k výpočtu dopravného nebo jiných poplatků za konkrétní objednávku nebo položku. Další informace, jak nastavit a používat rozšířené automatické náklady, naleznete v tématu [Omnikanálové rozšířené automatické náklady](./omni-auto-charges.md).

![Karta Objednávky zákazníka na stránce Parametry Commerce.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Aktualizace rozložení obrazovky transakcí v POS

Ujistěte se, že [rozložení obrazovky](./pos-screen-layouts.md) POS je nakonfigurováno tak, aby podporovalo vytváření a správu objednávek zákazníků a aby byly nakonfigurovány všechny požadované operace POS. Zde jsou některé z operací POS, které se doporučují ke správné podpoře vytváření a správy objednávek zákazníků:
- **Expedovat všechny produkty** – Tato operace slouží k zadání, že všechny řádky v košíku transakce budou expedovány do cílového místa.
- **Expedovat vybrané produkty** – Tato operace slouží k zadání, že vybrané řádky v košíku transakce budou expedovány do cílového místa.
- **Vyzvednout všechny produkty** – Tato operace slouží k zadání, že všechny řádky v košíku transakce budou vyzvednuty z vybraného umístění obchodu.
- **Vyzvednout vybrané produkty** – Tato operace slouží k zadání, že vybrané řádky v košíku transakce budou vyzvednuty z vybraného umístění obchodu.
- **Vyvézt všechny produkty** – Tato operace určuje, že budou vyvezeny všechny řádky v košíku transakce. Pokud je tato operace použita v POS, bude objednávka zákazníka převedena na transakci cash-and-carry.
- **Vyvézt vybrané produkty** – Tato operace slouží k určení, že vybrané řádky v košíku transakce si odnese zákazník v době nákupu. Tato operace je užitečná pouze u [hybridní objednávky](./hybrid-customer-orders.md).
- **Odvolat objednávku** – Tato operace se používá k vyhledání a načtení objednávek zákazníků, aby je uživatelé POS mohli podle potřeby upravovat, rušit nebo provádět operace související s plněním.
- **Změnit způsob dodání** – Tuto operaci lze použít k rychlé změně režimu dodání u řádků, které jsou již nakonfigurovány pro dodávku, aniž by uživatelé museli znovu projít tokem „expedovat všechny produkty“ nebo „expedovat vybrané produkty“.
- **Přepsání zálohy** – Tuto operaci lze použít ke změně částky zálohy, kterou zákazník zaplatí za vybranou objednávku zákazníka.

![Operace na obrazovce transakcí POS.](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Práce s objednávkami zákazníků v POS

> [!NOTE]
> Funkce rozpoznávání výnosů není aktuálně podporována pro použití v kanálech Commerce (e-commerce, POS, call centrum). Položky nakonfigurované s rozpoznáváním výnosů by neměly být přidávány k objednávkám vytvořeným v kanálech Commerce. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Vytvoření objednávky zákazníka pro produkty, které budou odeslány zákazníkovi

1. Na obrazovce transakce POS přidejte zákazníka do transakce.
2. Přidejte produkty do košíku.
3. Vyberte **Expedovat vybrané** nebo **Expedovat vše** k expedování produktů na adresu zákaznického účtu.
4. Vyberte volbu pro vytvoření objednávku zákazníka.
5. Potvrďte nebo změňte místo expedice, potvrďte nebo změňte dodací adresu a vyberte způsob dopravy.
6. Zadejte datum dodávky objednávky požadované zákazníkem.
7. Pomocí platebních funkcí můžete zaplatit veškeré vypočítané nesplacené částky nebo pomocí operace **Přepsání zálohy** změnit nesplacené částky a poté provést platbu.
8. Pokud nebyla zaplacena celá částka za objednávku, zadejte kreditní kartu, která bude zaznamenána pro zůstatek, který je nesplacen na objednávce, když je fakturována.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Vytvoření objednávky zákazníka pro produkty, které si zákazník vyzvedne

1. Na obrazovce transakce POS přidejte zákazníka do transakce.
2. Přidejte produkty do košíku.
3. Volbou **Vyzvednout vybrané** nebo **Vyzvednout vše** spusťe konfiguraci vyzvednutí objednávky.
4. Vyberte umístění obchodu, kde si zákazník vyzvedne vybrané produkty.
5. Vyberte datum, kdy bude položka vyzvednuta.
6. Pomocí platebních funkcí můžete zaplatit veškeré vypočítané nesplacené částky nebo pomocí operace **Přepsání zálohy** změnit nesplacené částky a poté provést platbu.
7. Pokud nebyla zaplacena celková částka objednávky, vyberte, zda zákazník poskytne platbu později (při vyskladnění), nebo zda bude kreditní karta nyní tokenizována a poté použita a zaznamenána v době vyskladnění.

### <a name="edit-an-existing-customer-order"></a>Úprava existující objednávky odběratele

Maloobchodní objednávky, které jsou vytvořeny v online kanálu nebo kanálu obchodu, lze podle potřeby odvolat a upravit prostřednictvím POS.

> [!IMPORTANT]
> Ne všechny maloobchodní objednávky lze upravovat prostřednictvím aplikace POS. Objednávky vytvořené v kanálu kontaktního střediska nelze upravovat prostřednictvím POS, pokud je pro kanál kontaktního střediska zapnuto nastavení [Povolit dokončení objednávky](./set-up-order-processing-options.md#enable-order-completion). Aby bylo zajištěno správné zpracování plateb, musí být objednávky, které pocházejí z kanálu kontaktního střediska a které používají funkci Povolit dokončení objednávky, upraveny prostřednictvím aplikace kontaktního střediska v centrále Commerce.

> [!NOTE]
> Doporučujeme, abyste neupravovali objednávky a nabídky v POS, které jsou vytvořeny uživatelem mimo call centrum v centrále Commerce. Tyto objednávky a nabídky nepoužívají cenový modul Commerce, takže pokud jsou upraveny v POS, cenový modul Commerce je přecení.


Ve verzi 10.0.17 a novější mohou uživatelé upravovat způsobilé objednávky prostřednictvím aplikace POS, i když je objednávka částečně splněna. Objednávky, které jsou plně fakturovány, však stále nelze upravovat prostřednictvím POS. Chcete-li tuto funkci aktivovat, zapněte funkci **Upravit částečně splněné objednávky v pokladním místě** v pracovním prostoru **Správa funkcí**. Pokud tato funkce není povolena nebo pokud používáte verzi 10.0.16 nebo starší, uživatelé budou moci upravovat objednávky zákazníků v POS pouze v případě, že je objednávka plně otevřená. Dále, pokud je funkce povolena, můžete omezit, které obchody mohou upravovat částečně splněné objednávky. Možnost zakázat tuto funkci pro konkrétní obchody lze konfigurovat prostřednictvím **Funkční profil** a pevné kartě **Všeobecné**.


1. Vyberte **Odvolat objednávku**.
2. Pomocí **vyhledávání** zadejte filtry a vyhledejte objednávku a poté vyberte **Použít**.
3. Vyberte objednávku v seznamu výsledků a poté vyberte **Upravit**. Pokud není dostupné tlačítko **Upravit**, objednávka je ve stavu, kdy ji nelze upravit.
4. V košíku transakce proveďte všechny nezbytné změny v objednávce zákazníka. Některé změny mohou být během úprav zakázány.
5. Dokončete proces úprav výběrem platební operace.
6. Chcete-li ukončit proces úprav bez uložení jakýchkoli změn, můžete použít operaci **Anulovat transakci**.

#### <a name="pricing-impact-when-orders-are-edited"></a>Vliv ceny na úpravu objednávek

Při zadávání objednávek v POS nebo na webu e-commerce Commerce se zákazníci zavazují k určité částce. Tato částka zahrnuje cenu a může také zahrnovat slevu. Zákazník, který zadá objednávku a později kontaktuje call centrum, aby tuto objednávku změnil (například aby přidal další položku), bude mít konkrétní očekávání ohledně uplatnění slev. I když platnost propagačních akcí na stávajících řádcích objednávky vyprší, zákazník bude očekávat, že slevy, které byly na tyto řádky původně uplatněny, zůstanou v platnosti. Pokud však při původním zadání objednávky nebyla uplatněna žádná sleva, ale od té doby sleva vstoupila v platnost, zákazník bude očekávat, že nová sleva bude uplatněna na změněnou objednávku. V opačném případě může zákazník pouze zrušit stávající objednávku a poté vytvořit novou objednávku, kde bude uplatněna nová sleva. Jak ukazuje tento scénář, musí být zachovány ceny a slevy, ke kterým se zákazníci zavázali. Uživatelé POS a call centra musí mít zároveň flexibilitu k přepočtu cen a slev na řádky prodejní objednávky podle potřeby.

Když jsou objednávky odvolávány a upravovány v POS, ceny a slevy stávajících řádků objednávek jsou považovány za „uzamčené“. Jinými slovy, nemění se, i když jsou některé řádky objednávky zrušeny nebo změněny nebo jsou přidány nové řádky objednávek. Chcete-li změnit ceny a slevy stávajících prodejních řádků, musí uživatel POS vybrat **Přepočítat**. Cenový zámek je poté odstraněn ze stávajících řádků objednávek. Před vydáním Commerce verze 10.0.21 však tato funkce nebyla v call centru k dispozici. Místo toho jakékoli změny řádků objednávek způsobily přepočítání cen a slev.

Ve verzi Commerce verze 10.0.21, nová funkce, která je pojmenována **Zabraňte neúmyslnému výpočtu ceny pro obchodní objednávky** je k dispozici v pracovním prostoru **Správa funkcí**. Ve výchozím nastavení je tato funkce zapnutá. Když je zapnutá, nová vlastnost **Cena uzamčena** je k dispozici pro všechny objednávky elektronického obchodování. Po dokončení zachycení objednávky u objednávek, které jsou zadány z jakéhokoli kanálu, je tato vlastnost automaticky povolena (to znamená, že je zaškrtnuto políčko) pro všechny řádky objednávky. Cenový modul Commerce pak vylučuje tyto řádky objednávek ze všech cen a slev výpočtů. Pokud je tedy objednávka upravena, řádky objednávky budou ve výchozím nastavení vyloučeny z výpočtu cen a slev. Uživatelé call centra však mohou vlastnost zakázat (tj. zrušit zaškrtnutí políčka) pro libovolný řádek objednávky a poté vybrat **Přepočítat** a zahrnout tak stávající řádky objednávek do cenových kalkulací.

I když na stávající prodejní řádek uplatňují manuální slevu, musí uživatelé call centra zakázat vlastnost **Cena uzamčena** prodejního řádku, než uplatní manuální slevu.

Uživatelé call centra mohou také zakázat vlastnost **Cena uzamčena** pro řádky objednávek hromadně výběrem **Odstranit cenový zámek** ve skupině **Vypočítat** na kartě **Prodej** v podokně akcí na stránce **Prodejní objednávka**. V tomto případě je cenový zámek odstraněn ze všech řádků objednávky kromě řádků, které nelze upravit (jinými slovy řádky, které mají stav **Částečně fakturováno** nebo **Fakturováno**). Poté, co jsou změny objednávky dokončeny a odeslány, je cenový zámek znovu použit na všechny řádky objednávky.

> [!IMPORTANT]
> Pokud je zapnutá funkce **Zabraňte neúmyslnému výpočtu ceny pro obchodní objednávky**, bude nastavení vyhodnocení obchodní smlouvy v pracovních postupech cen ignorováno. Jinými slovy, dialogová okna pro vyhodnocení obchodní dohody nezobrazí sekci **Související s cenou**. K tomuto chování dochází, protože nastavení hodnocení obchodní dohody a funkce cenového zámku mají podobný účel: zabránit neúmyslným změnám cen. Uživatelské prostředí pro hodnocení obchodní dohody se však u velkých objednávek, kde uživatelé musí vybrat jeden nebo více řádků objednávky pro přecenění, špatně přizpůsobuje.

> [!NOTE]
> Vlastnost **Cena uzamčena** lze deaktivovat pro jeden nebo více vybraných řádků pouze tehdy, když je použit modul **Call centrum**. Chování POS zůstává nezměněno. Jinými slovy, uživatel POS nemůže odemknout ceny pro vybrané řádky objednávek. Mohou však vybrat **Přepočítat** k odstranění zámku cen ze všech stávajících řádků objednávek.

### <a name="cancel-a-customer-order"></a>Zrušení objednávky zákazníka

1. Vyberte **Odvolat objednávku**.
2. Pomocí **vyhledávání** zadejte filtry a vyhledejte objednávku a poté vyberte **Použít**.
3. Vyberte objednávku v seznamu výsledků a poté vyberte **Zrušit**. Pokud není dostupné tlačítko **Zrušit**, objednávka je ve stavu, kdy ji již nelze zrušit.
4. Pokud jsou nakonfigurovány poplatky za zrušení, potvrďte je. Poplatky za zrušení můžete podle potřeby upravit, než je potvrdíte. 
5. V košíku transakce dokončete proces zrušení výběrem platební operace. Pokud zálohy, které byly zaplaceny, přesáhnou poplatek za zrušení, mohou vzniknout nesplacené refundace plateb.
6. Chcete-li ukončit proces zrušení bez uložení jakýchkoli změn, můžete použít operaci **Anulovat transakci**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Dokončení dodávky objednávky zákazníka nebo vyskladnění z POS

Po vytvoření objednávky bude zboží vyzvednuto zákazníkem z místa obchodu nebo expedováno v závislosti na konfiguraci objednávky. Další informace o tomto procesu najdete v dokumentaci k [plnění objednávky obchodu](./order-fulfillment-overview.md).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynchronní tok transakcí pro objednávky odběratele

Objednávky odběratele lze vytvořit v POS buď v synchronním nebo asynchronním režimu. Pokud při vytváření objednávek zákazníků v POS zaznamenáte problémy s výkonem nebo zpoždění uživatelů, zvažte zapnutí asynchronního vytváření objednávek.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Povolení vytvoření objednávky odběratele v asynchronním režimu

1. V centrále Commerce na stránce **Funkční profily** vyberte funkční profil, který odpovídá obchodu, který chcete konfigurovat.
2. Na pevné záložce **Obecné** nastavte možnost **Vytvořit objednávku odběratele v asynchronním režimu** na **Ano**.

Když je možnost **Vytvořit objednávku odběratele v asynchronním režimu** nastavena na **Ano**, objednávky odběratelů se vždy vytvářejí v asynchronním režimu, i když je k dispozici služba Retail Transaction Service (RTS). Pokud nastavíte tuto možnost na **Ne**, objednávky odběratelů jsou vždy vytvářeny v synchronním režimu pomocí služby RTS. Když jsou objednávky zákazníků vytvořeny v asynchronním režimu, jsou vyžádány a vytvořeny jako maloobchodní transakce v centrále Commerce z úloh na vyžádání (P). Odpovídající prodejní objednávky pro maloobchodní trasakce se vytvoří buď při ručním spuštění možnosti **Synchronizovat objednávky** nebo pomocí dávkového zpracování.

## <a name="additional-resources"></a>Další zdroje

[Hybridní objednávky zákazníka](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
