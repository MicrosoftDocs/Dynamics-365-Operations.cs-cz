---
title: Systémem řízený výdej v seskupení
description: Toto téma poskytuje přehled o systémem řízeném výdeji v seskupení v Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217234"
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

Nová položka nabídky mobilního zařízení se používá pro systémem řízené výdeje seskupení. ID profilu seskupení musí být zadáno pro možnost **Řízený dle**. Systémem řízené dotazy navíc může seskupit objednávky na základě specifických kritérií společnosti. Proto lze přiřazení pracovních objednávek dále optimalizovat určením vlastních kritérií řazení v pořadí dotazů řízeném systémem.

Po dokončení systémem řízeného výdeje v seskupení je pracovníkům skladu prezentováno seskupení, kde byly výdejové objednávky předem přiřazeny k pozici seskupení. Zaměstnanci proto mohou začít vybírat zboží pro více pracovních objednávek tím, že navštíví sklaové místo pouze jednou. Výdejní proces pro systémem řízený výdej v seskupení je stejný jako proces pro uživatelem řízený výdej v seskupení.

## <a name="set-up-system-directed-cluster-picking"></a>Vytvořit systémem řízený výdej v seskupení

### <a name="create-cluster-profiles"></a>Vytvořit profily seskupení

Profily seskupení řídí způsob, jakým systém vytváří jednotlivá seskupení. Pokud jsou vyžadována různá seskupení, měl by být pro každou položku nabídky mobilního zařízení vytvořen jiný profil seskupení.

1. Přejděte na **Řízení skladu \> Nastavení \> Mobilní zařízení \> Profily seskupení**.
2. Zvolte **Nové**.
3. Do pole **ID profilu seskupení** zadejte **2 pozice**.
4. Do pole **Název** zadejte **2 pozice**.
5. Na pevní záložce **Obecné** zadejte následující pole:

    - **Generovat ID seskupení:** nastavte tuto možnost na **Ano**. Tato možnost určuje, zda je ID seskupení automaticky vytvořeno systémem nebo zda jej uživatel vytvoří na začátku výdeje.
    - **Aktivovat pozice:** nastavte tuto možnost na **Ano**. Tato možnost určuje, zda jsou názvy pozic automaticky generovány na základě nastavení názvu pozice. Pokud tato možnost nastavena na **Ne**, použije se ID registrační značky pro pozici.
    - **Počet pozic:** vložte **2**. Toto pole určuje maximální počet pozic, které může seskupení mít (to znamená maximální počet polí, totů atd.).
    - **Název pozice:** vyberte **Numerická**, aby pozice byly pojmenovány pomocí souvislých čísel. Pokud vyberete **Abecední**, budou pozice pojmenovány v abecedním pořadí.
    - **Přerušit seskupení v:** vyberte **Vložit**. Toto pole určuje, kdy je seskupení přerušené.
    - **Typ ověření řazení:** vyberte **Skenování umístění**. Toto pole určuje, zda je ověřen krok zaskladnění.

6. Na pevné kartě **Řazení seskupené** můžete definovat kritéria řazení vytvořením nového řádku a nastavením následujících polí:

    - **Pořadové číslo:** toto pole určuje sekvenci, podle které je systém seřazen. Hodnota je zadána automaticky, můžete ji však podle potřeby změnit.
    - **Název pole:** vyberte **WMSLocationId**. Toto pole určuje pole, které tento řádek používá pro kritéria třídění.
    - **Řazení:** vyberte **vzestupně**. Toto pole určuje, zda se třídění provádí vzestupně nebo sestupně.

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

Chcete-li vytvořit novou položku nabídky mobilního zařízení pro výdej v seskupení řízeného systémem a propojit ID profilu clusteru s položkou nabídky mobilního zařízení, postupujte následovně.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
2. Zvolte **Nové**.
3. V poli **Název položky nabídky** zadejte **Seskupení SD**.
4. V poli **Nadpis** zadejte **Seskupení SD**.
5. V poli **Režim** vyberte **Práce**.
6. Nastavte hodnotu možnosti **Použít stávající práci** na **Ano**.
7. Na pevní záložce **Obecné** zadejte následující pole:

    - **Řídí:** vyberte **Řízeno systémem**.
    - Nastavte volbu **Generovat registrační značku vozidla** na **Ano**.
    - **ID profilu seskupení:** vyberte **2 pozice**.

8. Na pevné záložce **Pracovní třídy** nastavte platnou třídu práce pro tuto položku nabídky mobilního zařízení nastavením následujících polí:

    - **ID třídy práce:** Ujistěte se, že je zadán **Prodej**.
    - **Typ pracovního příkazu:** Ujistěte se, že je zadáno **Prodejní objednávky**.

9. Následujícím postupem zadáte nový dotaz na pracovní sekvenci řízenou systémem:

    1. Zvolte **Nové**.
    2. Do pole **Pořadové číslo** zadejte **1**.
    3. V poli **Popis** vyberte možnost **Priorita práce – ID práce**.

10. V nabídce vyberte příkaz **Upravit dotaz**.
11. Na kartě **Řazení** nastavte následující pole:

    - **Tabulka:** vyberte **Práce**.
    - **Odvozená tabulka:** vyberte **Práce**.
    - **Pole:** vyberte **Priorita práce**.
    - **Směr hledání:** vyberte **Vzestupné**.
    - **Tabulka:** vyberte **Práce**.
    - **Odvozená tabulka:** vyberte **Práce**.
    - **Pole:** vyberte **ID práce**.
    - **Směr hledání:** vyberte **Vzestupné**.

Systém nyní bude řadit ID práce v seskupení, nejprve podle priority práce a potom podle ID práce.

### <a name="set-up-a-mobile-device-menu"></a>Vytvořit nabídku mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
2. Přidejte položku nabídky, kterou jste právě vytvořili, do požadované nabídky.

## <a name="example"></a>Příklad

### <a name="create-picking-work"></a>Vytvořit práci výdeje

Dříve než můžete nastavit systémem řízený výdej v seskupení, musíte vytvořit nějakou způsobilou výstupní práci. Dříve vytvořený profil seskupení určuje dvě pozice clusteru. Proto je nutné vytvořit alespoň dvě ID práce.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
3. V poli **Účet odběratele** vyberte libovolného zákazníka.
4. Na pevné záložce **Obecné** v poli **Sklad** vyberte sklad **62**.
5. Vyberte **OK**.
6. Na pevné záložce **Řádky proejní objednávky** vyberte **Přidat řádek**.
7. V poli **Číslo položky** zvolte **A0001**.
8. Do pole **Množství** zadejte **1**.
9. Vyberte **Přidat řádek**, chcete-li přidat druhý řádek.
10. V poli **Číslo položky** zvolte **A0002**.
11. Do pole **Množství** zadejte **3**.
12. Zopakujte kroky 2 až 6.
13. V poli **Číslo položky** zvolte **A0001**.
14. Do pole **Množství** zadejte **4**.
15. Vyberte **Přidat řádek**, chcete-li přidat druhý řádek.
16. V poli **Číslo položky** zvolte **A0002**.
17. Do pole **Množství** zadejte **2**.

Rezervace zásob a jejich uvolnění do skladu. Vytvoří se dvě různé ID práce. Každé ID práce má dva řádky výdeje.

### <a name="run-the-mobile-device-flow"></a>Spustit tok mobilního zařízení

1. V mobilním zařízení vyberte nabídku obsahující novou položku nabídky mobilního zařízení.
2. Vyberte položku **SD seskupení** a zahajte výdej. Vytvoří se seskupení a k němu jsou připojeny dvě dříve vytvořené ID práce. Pokud jste vytvořili více než dvě ID práce, budou do seskupení přidány pouze první dvě. Všimněte si, že ID práce jsou přidávané do seskupení ve vzestupném pořadí, jak jste určili v nastavení dotazu.

    > [!NOTE]
    > Nové seskupení je vytvořeno automaticky pouze v případě, že již byly vytvořeny dodatečné další ID práce. V opačném případě se zobrazí následující zpráva: pro seskupení nelze najít dostatek práce.

    Po výběru nabídky se zobrazí první obrazovka pro vyskladnění. Systém agreguje všechny odpovídající řádky výdeje ze dvou ID práce a přesměruje vás na místo vyskladnění, abyste mohli obě objednávky uspokojit pomocí jednoho vyskladnění. Tento proces se provádí stejným způsobem jako proces při výběru seskupení řízeného uživatelem.

3. Potvrďte první vyskladnění. Poté musíte zadat název pozice pro potvrzení, že bylo zboží umístěno na správné místo.
4. Tento postup opakujte, dokud nebudou všechny položky vyskladněny a umístěny do správné pozice.
5. Posledním krokem mobilního zařízení je umístit seskupení do konečného umístění. Po potvrzení této operace je seskupení uzavřeno a přerušeno, a to na základě hodnoty, kterou jste nastavili pro pole **Přerušit seskupení v** v profilu seskupení. ID práce jsou také uzavřeny.
6. V mobilním zařízení je zobrazena zpráva "Seskupení dokončeno".
