---
title: Systémem řízený výdej v seskupení
description: Toto téma poskytuje přehled o systémem řízeném výdeji v seskupení v Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0838405bcb5ee0d8e582093fbbd69553228cb2b6
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424204"
---
# <a name="system-directed-cluster-picking"></a>Systémem řízený výdej v seskupení

[!include [banner](../includes/banner.md)]

Výdej v seskupení je proces výdeje, který umožňuje vybrat položky pro více objednávek současně, a to jejich seskupením pro výběr. Musíte tak místo vyskladnění navštívit pouze jednou. Tato funkce se obvykle používá s malými výdeji objednávek nebo s množstvím, které je menší než množství v balení.

Je-li nastaven systémem řízený výdej v seskupení, můžete v závislosti na systému vytvořeném seskupení vybrat záhlaví práce pro výdej v seskupení. Systém vydává seskupení objednávek až do počtu pozic zadaných v profilu seskupení. Proto je možné vybrat více objednávek současně, aniž by bylo nutné vytvořit seskupení ručně.

Systémem řízený výdej v seskupení nabízí alternativu k ručnímu vytváření seskupení, kde je k vytvoření seskupení použit profil seskupení. Před použitím profilu seskupení je nutné definovat několik řádků souvisejících s nastavením:

- **Počet pozic** odpovídá počtu objednávek, které budou do seskupení vloženy. Proto odpovídá počtu totů.
- **Přerušit seskupení** určuje, kdy má být seskupení přerušené.
- **Generovat ID seskupení** určuje, zda bude ID seskupení generován systémem nebo zadán uživatelem.
- **Typ ověření řazení** určuje, zda je vyžadováno ověření polohy.

Nová položka nabídky mobilního zařízení se používá pro systémem řízené výdeje seskupení. Pro vybranou možnost **Řídí** musí být zadáno **ID profilu clusteru**. Systémem řízené dotazy klasifikace práce navíc mohou seskupit objednávky na základě specifických kritérií společnosti. Proto lze přiřazení pracovních příkazů dále optimalizovat určením individuálně nastavený kritérií řazení v pořadí dotazů řízeném systémem.

Po povolení systémem řízeného výdeje v seskupení je pracovníkům skladu prezentováno seskupení, kde byly výdejové objednávky předem přiřazeny k pozici seskupení. Zaměstnanci proto mohou začít vybírat zboží pro více pracovních objednávek tím, že navštíví sklaové místo pouze jednou. Výdejní proces pro systémem řízený výdej v seskupení je stejný jako proces pro uživatelem řízený výdej v seskupení.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Povolte funkci výběru clusteru zaměřenou na systém

Než budete moci použít tuto funkci, musíte ji povolit ve svém systému. Správci mohou pomocí stránky [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. Tato funkce je uvedena jako:

- **Modul** - Řízení skladu
- **Název funkce** - výběr clusteru zaměřený na systém

Tato funkce také vyžaduje povolení závislé funkce. Závislá funkce je:

- **Modul** - Řízení skladu
- **Název funkce** - Systémově řízené sekvenční práce v rámci celé organizace

## <a name="set-up-system-directed-cluster-picking"></a>Vytvořit systémem řízený výdej v seskupení

### <a name="create-cluster-profiles"></a>Vytvořit profily seskupení

Profily seskupení řídí způsob, jakým systém vytváří jednotlivá seskupení. Pokud jsou vyžadována různá seskupení, měl by být pro každou položku nabídky mobilního zařízení vytvořen jiný profil seskupení.

1. Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.
2. Zvolte **Nové**.
3. Do pole **ID profilu seskupení** zadejte **2 pozice**.
4. Do pole **Název** zadejte **2 pozice**.
5. Na pevné záložce **Obecné** zadejte následující informace:

    - **Generovat ID clusteru** - Vyberte **Ano**. Tato možnost určuje, zda je ID seskupení automaticky vytvořeno systémem nebo zda jej uživatel vytvoří na začátku výdeje. 
    - **Aktivovat pozice** - Vyberte **Ano**. Tato možnost určuje, zda jsou názvy pozic automaticky generovány na základě nastavení názvu pozice. Pokud tato možnost nastavena na **Ne**, použije se ID registrační značky pro pozici.
    - **Počet pozic** - Vyberte **2**. Toto pole určuje maximální počet pozic, které může seskupení mít (to znamená maximální počet polí, totů atd.).
    - **Název pozice:** Vyberte **Numerická**, aby pozice byly pojmenovány pomocí souvislých čísel. Pokud vyberete **Abecední**, budou pozice pojmenovány v abecedním pořadí.
    - **Přerušit seskupení v-** vyberte **Vložit**. Toto pole určuje, kdy je seskupení přerušené. 
    - **Typ ověření řazení-** vyberte **Skenování umístění**. Toto pole určuje, zda je ověřen krok zaskladnění.
        
6. Na pevné záložce **Řazení clusteru** můžete definovat kritéria řazení vytvořením nového řádku a zadáním následujících informací:

    - **Pořadové číslo** - Vyberte **1**. Toto pole určuje pořadí, podle kterého systém třídí. Hodnota je zadána automaticky, můžete ji však podle potřeby změnit.
    - **Název pole:** zadejte **WMSLocationId**. Toto pole určuje pole, které tento řádek používá pro kritéria třídění.
    - **Řazení-** vyberte **vzestupně**. Toto pole určuje, zda se třídění provádí vzestupně nebo sestupně.

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

Chcete-li vytvořit novou položku nabídky mobilního zařízení pro výdej v seskupení řízeného systémem a propojit ID profilu clusteru s položkou nabídky mobilního zařízení, postupujte následovně.

1. Přejděte do nabídky **Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení**.
1. Zvolte **Nové**.
1. V části záhlaví zadejte následující informace:
    - **Název položky nabídky** - Cluster SD
    - **Název** - SD Cluster
    - **Režim** - Práce
    - **Použít existující práci** - Ano

1. Na pevné záložce **Obecné** zadejte následující informace:
    - **Řídí** -Systémem řízený výdej v seskupení
    - **Generovat registrační značky** - Ano
    - **ID profilu seskupení** - 2 pozice.

1. Na pevné záložce **Pracovní třídy** nastavte platnou třídu práce pro tuto položku nabídky mobilního zařízení nastavením následujících polí:
    - **ID pracovní třídy** - Prodeje
    - **Typ pracovního příkazu** - Prodejní objednávky

1. V podokně akcí **Položky nabídky mobilního zařízení** vyberte **Systémově orientované dotazy na pracovní posloupnosti** a podle těchto kroků určete nový dotaz pracovního pořadí směrovaný systémem:
    - V podokně akcí vyberte **Nový**.
    - **Pořadové číslo** - 1
    - **Popis** - Priorita práce - ID práce

1. V podokně akcí vyberte **Upravit dotaz**.
1. Vyberte kartu **Řazení**.
1. Vyberte **Přidat** pro přidání nového řádku, potom zadejte následující:
    - **Tabulka** - Práce
    - **Odvozená tabulka** - Práce
    - **Pole** - Priorita práce.
    - **Směr hledání** - Vzestupné.
1. Vyberte **Přidat** pro přidání druhého řádku, potom zadejte následující:
    - **Tabulka** - Práce
    - **Odvozená tabulka** - Práce
    - **Pole** - ID práce
    - **Směr hledání** - Vzestupné.

1. Systém nyní bude řadit ID práce v seskupení, nejprve podle priority práce a potom podle ID práce.

### <a name="set-up-a-mobile-device-menu"></a>Vytvořit nabídku mobilního zařízení

1. Přejděte do nabídky **Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení**.
1. Přidejte položku nabídky **Seskupení SD**, kterou jste právě vytvořili, do nabídky Mobilní zařízení.
1. Vyberte nabídku **Odchozí**.
1. V podokně akcí vyberte **Upravit**.
1. Rolujte, dokud nenajdete **Seskupení SD**.
1. Vyberte **Seskupení SD**, šipka směřující na seznam **Struktura nabídky** se aktivuje.
1. Výběrem tlačítka se **šipkou** přesuňte položku nabídky **Seskupení SD** do struktury nabídky **Odchozí**.
1. Vyberte **Seskupení SD** ze seznamu **Struktura nabídky** a pak pomocí šipky **NAHORU** nebo **DOLů** přesuňte položku nabídky do požadované pozice v nabídce mobilního zařízení.

## <a name="scenario"></a>Scénář

### <a name="create-picking-work"></a>Vytvořit práci výdeje

Dříve než můžete nastavit systémem řízený výdej v seskupení, musíte vytvořit způsobilou výstupní práci. Dříve vytvořený profil seskupení určuje dvě pozice clusteru. Proto je nutné vytvořit alespoň dvě ID práce. V tomto scénáři vytvoříte dvě prodejní objednávky, rezervujete zásoby, uvolníte prodejní objednávky do skladu a poté ručně zpracujete vlnu.

1. Přejděte na **Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
1. V podokně akcí vyberte **Nový** k vytvoření první prodejní objednávky.
    - Otevře se nabídka **Vytvořte prodejní objednávku**, zadejte následující informace:
        - Na pevné záložce **Zákazník** zadejte **Účet zákazníka** - **US-004**.
        - Na pevné záložce **Obecné** zadejte **Sklad** - **62**.
        - Vyberte **OK** k zavření nabídky a vytvoření prodejní objednávky.
    - Na pevné záložce **Řádky prodejní objednávky** vyberte **Přidat řádek**, pokud není automaticky přidán nový řádek, a zadejte následující:
        - **Číslo položky** - A0001
        - **Množství** - 1
        - Vyberte **Přidat řádek**, chcete-li přidat druhý řádek.
        - **Číslo položky** - A0002
        - **Množství** - 3
    - Rezervujte zásoby pro oba řádky, které jste právě vytvořili.
        - Vyberte **Řádek 1**.
        - V podokně akcí **Řádky prodejní objednávky** vyberte **Zásoby** a ze seznamu vyberte **Rezervace**.
        - Ve formuláři **Rezervace** vyberte **Rezervovat šarži** k rezervování zásob.
        - Po dokončení rezervace zavřete formulář **Rezervace**.
        - Opakujte tyto kroky, abyste rezervovali zásoby pro **Řádek 2**.
1. V podokně akcí vyberte **Nový** k vytvoření druhé prodejní objednávky.
    - Otevře se nabídka **Vytvořte prodejní objednávku**, zadejte následující informace:
        - Na pevné záložce **Zákazník** zadejte **Účet zákazníka** - **US-005**.
        - Na pevné záložce **Obecné** zadejte **Sklad** - **62**.
        - Vyberte **OK** k zavření nabídky a vytvoření prodejní objednávky
    - Na pevné záložce **Řádky prodejní objednávky** vyberte **Přidat řádek**, pokud není automaticky přidán nový řádek, a zadejte následující informace:
        - **Číslo položky** - A0001
        - **Množství** - 4
        - Vyberte **Přidat řádek**, chcete-li přidat druhý řádek.
        - **Číslo položky** - A0002
        - **Množství** - 2
    - Rezervujte zásoby pro oba řádky, které jste právě vytvořili.
        - Vyberte **Řádek 1**.
        - V podokně akcí **Řádky prodejní objednávky** vyberte **Zásoby** a ze seznamu vyberte **Rezervace**.
        - Ve formuláři **Rezervace** vyberte **Rezervovat šarži** k rezervování zásob.
        - Po dokončení rezervace zavřete formulář **Rezervace**.
        - Opakujte tyto kroky, abyste rezervovali zásoby pro **Řádek 2**.
    - Zavřete prodejní objednávku a vraťte se na stránku se seznamem **Všechny prodejní objednávky**.
1. Vyhledejte právě vytvořené dvě prodejní objednávky (možná budete muset stránku obnovit). V tabulce vyberte obě prodejní objednávky pomocí zaškrtávacího políčka sekce.
    - V podokně akcí **Všechny prodejní objednávky** vyberte kartu **Sklad**.
    - Ve skupině **Akce** vyberte **Vydat do skladu** pro vydání obou prodejních objednávek do skladu.
1. Po dokončení procesu uvolnění do skladu se zobrazí informační zpráva.
    - Pro každou prodejní objednávku budou vytvořeny zásilky.
    - Bude vytvořena vlna a obě zásilky budou přiřazeny vlně. Poznamenejte si **ID vlny**.
1. Přejděte na **Řízení skladu > Výstupní vlny > Vlny dodávek > Všechny vlny**.
    - V seznamu **Všechny vlny** najděte a vyberte **ID vlny**, které jste vytvořili v předchozím kroku.
    - Vyberte tlačítko **Vlna** v podokně akcí.
    - Ve skupině **Vlna** vyberte **Zpracovat** ke zpracování vlny, a vyberte **Práce**.
    - Informační zprávy budou generovány po dokončení zpracování, což znamená, že práce byla vytvořena a vlna byla zaúčtována.
1. **Volitelné**: Přejděte na **Řízení skladu > Práce > Detaily práce** pro zobrazení vytvořené práce. Vytvoří se dvě různé ID práce. Každé ID práce má dva řádky výdeje.

### <a name="run-the-mobile-device-flow"></a>Spustit tok mobilního zařízení

1. Přihlaste se do mobilního zařízení pro uživatele ve skladu **62**.
1. V **hlavní nabídce** vyberte **Odchozí**.
1. V nabídce **Odchozí** vyberte **Seskupení SD** pro zahájení výběru.
    - Vytvoří se seskupení a k němu jsou připojena dvě dříve vytvořená ID práce. Pokud jste vytvořili více než dvě ID práce, budou do seskupení přidány pouze první dvě. Všimněte si, že ID práce jsou přidávané do seskupení ve vzestupném pořadí, jak jste určili v nastavení dotazu.

    > [!NOTE]
    > Nové seskupení je vytvořeno automaticky pouze v případě, že již byly vytvořeny dodatečné další ID práce. V opačném případě se zobrazí následující zpráva: pro seskupení nelze najít dostatek práce.

    - Po výběru nabídky se zobrazí první obrazovka pro vyskladnění. Systém agreguje všechny odpovídající řádky výdeje ze dvou ID práce a přesměruje vás na místo vyskladnění, abyste mohli obě objednávky uspokojit pomocí jednoho vyskladnění. Tento proces se provádí stejným způsobem jako proces při výběru seskupení řízeného uživatelem.

1. Potvrďte první místo výběru a položku výběrem **OK**.
    - Množství výběru bude součet položky zobrazené na prodejních objednávkách v seskupení.
1. Zadejte název pozice (číselný nebo abecední) a potvrďte, že množství položky vybrané pro danou pozici bylo umístěno na správnou pozici.
1. Tento postup opakujte, dokud nebudou všechna množství položek vyskladněna a umístěna do správné pozice.
1. Posledním krokem mobilního zařízení je **umístit** seskupení do konečného umístění. Vyberte **OK**
    - Po potvrzení této operace je seskupení uzavřeno a přerušeno, a to na základě hodnoty, kterou jste nastavili pro pole **Přerušit seskupení v** v profilu seskupení. ID práce jsou také uzavřeny.
1. V mobilním zařízení je zobrazena zpráva "Seskupení dokončeno".


[!INCLUDE[footer-include](../../includes/footer-banner.md)]