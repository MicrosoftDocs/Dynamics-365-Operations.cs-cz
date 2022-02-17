---
title: Čárové kódy GS1 a QR kódy
description: Toto téma popisuje, jak nastavit čárové kódy GS1 a QR kódy, aby bylo možné ve skladu skenovat štítky.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 702985ef9726690829e35e43d270477be318fc41
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075207"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>Čárové kódy GS1 a QR kódy

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- Preview until 10.0.25 GA -->

Pracovníci ve skladech musí často dokončit několik úkolů, když pomocí skeneru mobilního zařízení registrují pohyby položky, palety nebo kontejneru. Tyto úkoly mohou zahrnovat jak skenování čárových kódů, tak ruční zadávání informací na mobilním zařízení. Čárové kódy používají formát specifický pro určitou společnost, který definujete a spravujete ve službě Microsoft Dynamics 365 Supply Chain Management.

Formáty čárových kódů GS1 a QR kódů pro přepravní štítky byly vyvinuty tak, aby poskytovaly globální standard pro výměnu dat mezi společnostmi. Formáty GS1 kódují data, ale také vám umožňují použít předdefinovaný seznam *identifikátorů aplikace* k definici významu dat. Standard GS1 definuje formát dat a různé druhy dat, která lze použít ke kódování. Na rozdíl od starších čárových kódů mohou mít čárové kódy GS1 více datových prvků. Naskenování jednoho čárového kódu proto může zachytit několik typů informací o produktu, jako je dávka a datum vypršení platnosti.

Podpora GS1 ve službě Supply Chain Management dramaticky zjednodušuje proces skenování ve skladech, kde jsou palety a kontejnery označeny pomocí kódů ve formátu GS1. Pracovníci skladu mohou extrahovat všechny požadované informace pomocí jediného skenování čárového kódu GS1. Čárové kódy GS1 eliminují nutnost provádět vícenásobné skenování a/nebo ručně zadávat informace a pomáhají tak zkrátit čas spojený s úkoly. Současně také pomáhají zlepšit přesnost.

Správci logistiky musí nastavit požadovaný seznam identifikátorů aplikací a každý z nich přiřadit k příslušným položkám nabídky mobilního zařízení. Identifikátory aplikace pak lze použít napříč sklady jako globální nastavení pro účely stěhování a balení. Všechny přepravní štítky proto budou mít jednotnou formu.

Pokud není uvedeno jinak, toto téma používá výraz *čárový kód* jako odkaz na čárové kódy i QR kódy.

## <a name="turn-on-the-gs1-feature"></a>Zapnutí funkce GS1

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Skenování čárových kódů GS1*

## <a name="set-up-global-gs1-options"></a>Nastavení globálních možností GS1

Stránka **Parametry správy skladu** nabízí několik nastavení, která vytvářejí globální možnosti GS1.

Chcete-li nastavit globální možnosti GS1, postupujte následujícím způsobem.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na záložce **Čárové kódy** vyplňte následující pole:

    - **Znak FNC1** – Zadejte znaky, které mají být při analýze čárového kódu interpretovány jako předpona.
    - **Znak datové matice** – Zadejte znaky, které mají být při analýze datové matice interpretovány jako předpona.
    - **Znak QR kódu** – Zadejte znaky, které mají být při analýze QR kódu interpretovány jako předpona.
    - **Oddělovač skupin** – Zadejte znak, který identifikuje oddělené části čárového kódu nebo QR kódu.
    - **Maximální délka identifikátoru** – Zadejte maximální počet znaků, který je povolen v identifikátoru aplikace.

> [!NOTE]
> Předpony systému sdělují, že čárový kód je šifrován podle standardu GS1. Současně a pro různé účely lze použít až tři předpony (**Znak FNC1**, **Znak datové matice** a **Znak QR kódu**).

## <a name="gs1-application-identifiers"></a>Identifikátory aplikace GS1

Formáty GS1 kódují data, ale také vám umožňují použít předdefinovaný seznam identifikátorů aplikace k definici významu dat. Správci logistiky musí nastavit požadovaný seznam identifikátorů aplikací a každý z nich přiřadit k příslušným položkám nabídky mobilního zařízení. Identifikátory pak lze použít napříč sklady jako globální nastavení pro účely stěhování a balení. Všechny přepravní štítky proto budou mít jednotnou formu.

Systém používá data, zejména předdefinované identifikátory aplikací, ke stanovení pravidel, která by měla být použita na příslušnou naskenovanou informaci.

Každý identifikátor aplikace signalizuje systému, že následující znaky v naskenovaném čárovém kódu by měly být považovány za blok zašifrovaných informací. Nastavení identifikátorů aplikace definuje, jak má systém interpretovat čárový kód a uložit jej jako hodnotu v systému.

Manažeři logistiky mohou používat standardní mezinárodní identifikátory aplikací a/nebo si vytvářet vlastní.

### <a name="load-the-standard-application-identifiers"></a>Načtení standardních identifikátorů aplikace

Chcete-li rychle začít, můžete načíst seznam běžných mezinárodních identifikátorů aplikací. Seznam pak můžete podle potřeby později rozšířit nebo upravit.

Chcete-li načíst standardní identifikátory aplikace, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Identifikátory aplikace GS1**.
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**.

> [!WARNING]
> Příkaz **Vytvořit výchozí nastavení** odstraní všechny aktuálně definované identifikátory aplikace a nahradí je standardním seznamem. Po načtení výchozího nastavení však můžete seznam přizpůsobit podle potřeby.

### <a name="set-up-custom-application-identifiers"></a>Nastavení vlastních identifikátorů aplikací

Pokud se některé nebo všechny identifikátory aplikací, které vaše společnost používá, liší od standardní sady, můžete vytvořit vlastní kódy od nuly nebo upravit standardní sadu podle potřeby.

Chcete-li nastavit a přizpůsobit vlastní identifikátory aplikace GS1, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Identifikátory aplikace GS1**.
1. Proveďte jeden z následujících kroků:

    - Chcete-li vytvořit nový identifikátor: v podokně Akce vyberte **Nový** .
    - Chcete-li upravit existující identifikátor: Vyberte identifikátor a poté v podokně akcí vyberte **Upravit**.

1. Nastavte následující pole pro nový nebo vybraný identifikátor:

    - **Identifikátor aplikace** – Zadejte identifikační kód pro identifikátor aplikace. Tento kód je obvykle dvouciferné celé číslo, ale může být i delší. U desetinných hodnot udává poslední číslice počet desetinných míst. Další informace najdete v popisu zaškrtávacího políčka **Desetinné** později v tomto seznamu.
    - **Popis** – Zadejte krátký popis identifikátoru.
    - **Pevná délka** – Toto políčko zaškrtněte, pokud hodnoty, které jsou skenovány pomocí tohoto identifikátoru aplikace, mají pevný počet znaků. Pokud je délka hodnot proměnná, zrušte zaškrtnutí tohoto políčka. V tomto případě musíte zadat konec hodnoty pomocí znaku oddělovače skupin, který jste zadali na stránce **Parametry správy skladu**.
    - **Délka** – Zadejte maximální počet znaků, které se mohou objevit v hodnotách naskenovaných pomocí tohoto identifikátoru aplikace. Pokud je zaškrtnuto políčko **Pevná délka**, očekává se přesně tento počet znaků.
    - **Typ** – Vyberte typ hodnoty, která se má skenovat pomocí tohoto identifikátoru aplikace (*Číselný*, *Alfanumerický* nebo *Datum*). U kalendářních dat je očekávaný formát RRMMDD (bez mezer a spojovníků).
    - **Desetinný** – Toto políčko zaškrtněte, pokud hodnota obsahuje implicitní desetinnou čárku. Pokud je toto pole zaškrtnuto, systém použije k určení počtu desetinných míst poslední číslici identifikátoru aplikace. Pokud má identifikátor aplikace hodnotu například *3205*, pět číslic nejvíce vpravo od hodnoty bude interpretováno jako následující za desetinnou čárkou.

> [!NOTE]
> Oddělovač skupin, který je uveden na stránce **Parametry správy skladu** je volitelný, pokud má hodnota, za kterou následuje identifikátor aplikace, pevnou délku nebo pokud je její délka maximalizována (tj. pokud se délka rovná hodnotě **Délka**, která je nastavena pro identifikátor aplikace).

## <a name="establish-the-generic-gs1-setup"></a>Vytvoření obecného nastavení GS1

Obecné nastavení GS1 vytváří kolekci běžných mapování. Tato mapování srovnají každé relevantní vstupní pole v mobilní aplikaci s identifikátorem aplikace, který řídí, jak by měly být hodnoty z naskenovaných čárových kódů interpretovány a ukládány do tohoto pole. Ve výchozím nastavení se tato nastavení vztahují na všechna skenování pro všechny položky nabídky mobilního zařízení. Lze je však přepsat pro jedno nebo více konkrétních polí zásadou GS1, která je přiřazena konkrétní položce nabídky.

Obecné nastavení GS1 umožňuje skenovat pouze jednu hodnotu najednou. Pokud tedy chcete načíst více hodnot polí z jednoho skenování, musíte pro příslušné položky nabídky nastavit zásadu GS1.

Další informace o zásadách GS1 naleznete v další části.

### <a name="load-the-standard-generic-gs1-setup"></a>Načtení standardního obecného nastavení GS1

Stránka **Obecné nastavení GS1** umožňuje načíst standardní sadu mapování mezi poli mobilního zařízení a standardními identifikátory aplikace, které jsou vytvořeny výchozím nastavením.

Chcete-li vytvořit obecné nastavení GS1, přejděte na nabídku **Správa skladu \> Nastavení \> GS1 \> Obecné nastavení GS1**. Poté vyberte příkaz **Vytvořit výchozí nastavení**, aby se automaticky přiřadil vhodný identifikátor aplikace ke každému poli, které obvykle používají položky nabídky mobilního zařízení.

> [!WARNING]
> Pokud již nějaké obecné nastavení GS1 existuje, příkaz **Vytvořit výchozí nastavení** jej zcela odstraní a načte standardní nastavení.

### <a name="customize-the-standard-generic-gs1-setup"></a>Přizpůsobení standardního obecného nastavení GS1

Chcete-li přizpůsobit obecné nastavení GS1, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Obecné nastavení GS1**.
1. Proveďte jeden z následujících kroků:

    - Vytvoření nového mapování: V podokně Akce vyberte možnost **Nová**.
    - Chcete-li upravit existující mapování: Vyberte mapování a poté v podokně akcí vyberte **Upravit**.

1. Nastavte následující pole pro nové nebo vybrané mapování:

    - **Pole** – Vyberte nebo zadejte vstupní pole mobilní aplikace, ke kterému má být přiřazena příchozí hodnota. Hodnota není zobrazovaný název, který vidí pracovníci. Je to název klíče, který je přiřazen poli v podkladovém kódu. Výchozí nastavení poskytuje kolekci polí, která budou pravděpodobně užitečná, a obsahuje intuitivní názvy klíčů pro každé pole a odpovídající naprogramované funkce. Možná však budete muset promluvit se svými vývojovými partnery, abyste našli správný výběr pro vaši implementaci.
    - **Identifikátor aplikace** – Vyberte příslušný identifikátor aplikace, jak je definován na stránce **Identifikátory aplikace GS1**. Identifikátor určuje, jak bude čárový kód interpretován a uložen jako hodnota pojmenovaného pole. Poté, co vyberete identifikátor aplikace, zobrazí pole **Popis** jeho popis.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Nastavení zásad GS1, které můžete přiřadit k položkám nabídky mobilního zařízení

Účelem standardu GS1 je umožnit pracovníkům načíst najednou několik hodnot při skenování jednoho čárového kódu. K dosažení tohoto cíle musejí logističtí manažeři nastavit zásady GS1, které systému řeknou, jak interpretovat vícehodnotové čárové kódy. Později můžete k položkám nabídky mobilního zařízení přiřadit zásady a řídit tak, jak bude čárový kód interpretován, když jej pracovníci skenují prostřednictvím konkrétní položky nabídky.

Pokud k položce nabídky není přiřazena žádná zásada GS1, systém může zachytit pouze jednu hodnotu. Tato hodnota je použita na vstupu mobilní aplikace, který je vybrán, když pracovník provede skenování, jak je uvedeno v obecném nastavení GS1. Pokud je k položce nabídky přiřazena zásada GS1, systém stále používá obecné nastavení GS1 k mapování první hodnoty čárového kódu do vybraného pole. Může však poté zachytit další hodnoty polí, jak je uvedeno v příslušných zásadách.

### <a name="load-the-standard-specific-gs1-policies"></a>Načtení standardních specifických zásad GS1

Chcete-li začít rychle, můžete načíst sadu zásad GS1. Zásady pak můžete podle potřeby později rozšířit nebo upravit.

Chcete-li načíst standardní identifikátory aplikace, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> GS1 \> Zásada GS1**.
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**.

> [!WARNING]
> Příkaz **Vytvořit výchozí nastavení** odstraní všechny aktuálně definované zásady a nahradí je standardní sadou zásad. Po načtení výchozího nastavení však můžete zásady přizpůsobit podle potřeby.

### <a name="set-up-custom-specific-gs1-policies"></a>Nastavení vlastních specifických zásad GS1

Chcete-li nastavit a přizpůsobit své zásady GS1, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> GS1 \> Zásada GS1**.
1. Proveďte jeden z následujících kroků:

    - Vytvoření nové zásady: V podokně Akce vyberte možnost **Nová**.
    - Chcete-li upravit existující zásadu, vyberte ji v podokně seznamu.

1. V záhlaví nové nebo vybrané zásady nastavte následující pole:

    - **Název zásady** – Zadejte název zásady.
    - **Popis** – Zadejte krátký popis zásady.

1. Na záložce pod záhlavím namapujte názvy polí na identifikátory aplikace podle toho, jak to vyžaduje aktuální zásada. Pomocí tlačítek na panelu nástrojů můžete podle potřeby přidávat a odebírat řádky. Pro každý řádek je třeba nastavit tato pole:

    - **Pole** – Vyberte nebo zadejte vstupní pole mobilní aplikace, ke kterému má být přiřazena příchozí hodnota. Hodnota není zobrazovaný název, který vidí pracovníci. Je to název klíče, který je přiřazen poli v podkladovém kódu. Výchozí nastavení poskytuje kolekci polí, která budou pravděpodobně užitečná, a obsahuje intuitivní názvy klíčů pro každé pole a odpovídající naprogramované funkce. Možná však budete muset promluvit se svými vývojovými partnery, abyste našli správný výběr pro vaši implementaci.
    - **Identifikátor aplikace** – Vyberte příslušný identifikátor aplikace, jak je definován na stránce **Identifikátory aplikace GS1**. Identifikátor určuje, jak bude čárový kód interpretován a uložen jako hodnota pojmenovaného pole. Poté, co vyberete identifikátor aplikace, zobrazí pole **Popis** jeho popis.
    - **Třídění** – Každý vícehodnotový čárový kód obsahuje řadu identifikátorů aplikace a za každým z nich následuje hodnota. Příslušná zásada GS1 určuje, jak jsou jednotlivé identifikátory aplikace namapovány na pole databáze. Pokud však čárový kód používá stejný identifikátor aplikace více než jednou, systém při jejich mapování na pole použije pořadí, ve kterém se identifikátory aplikací objeví v kódu. U řádků, které sdílejí identifikátor aplikace s jedním nebo více dalšími řádky, použijte toto pole k určení pořadí, ve kterém se zpracovávají odpovídající řádky. Nejprve bude zpracován řádek, který má nejnižší hodnotu řazení.

> [!NOTE]
> U čárových kódů, které obsahují více než jeden identický identifikátor aplikace, *musíte* použít pole **Třídění** pro stanovení pořadí polí.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Přiřazení zásad GS1 k položkám nabídky mobilního zařízení

Ve výchozím nastavení všechny položky nabídky mobilního zařízení poskytují vstupní pole, kde mohou pracovníci skenovat jednu hodnotu podle obecného nastavení GS1. Pokud chcete, aby pracovníci mohli skenovat více než jednu hodnotu pole v jednom skenování pro libovolnou položku nabídky mobilního zařízení, musíte přiřadit zásady GS1 podle těchto kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vytvořte nebo otevřete položku nabídky.
1. Na záložce **Všeobecné** nastavte pole **Zásada GS1** na zásadu, která se vztahuje na položku nabídky.

## <a name="gs1-setup-example"></a>Příklad nastavení GS1

Tento příklad platí pro systém, kde jsou možnosti GS1 nastaveny následujícím způsobem:

- Na stránce **Parametry správy skladu** se vytvoří následující globální nastavení:

  - **Znak FNC1:** *\]C1*
  - **Oddělovač skupin:** *\~*

- Na stránce **Identifikátory aplikace GS1** jsou pro tento příklad relevantní následující identifikátory aplikace.

    | Identifikátor aplikace | popis | Pevná délka | Délka | Typ | Desetinné |
    |---|---|---|---|---|---|
    | 01 | Číslo GTIN | Vybrané | 14 | Číselné | Proplaceno |
    | 10 | Číslo dávky | Proplaceno | 20 | Alfanumerické | Proplaceno |
    | 17 | Datum vypršení platnosti | Vybrané | 6 | Datum | Proplaceno |
    | 30 | Přijaté množství | Proplaceno | 8 | Číselné | Proplaceno |

- Na stránce **Obecné nastavení GS1** jsou pro tento příklad relevantní následující nastavení pro obecné zásady GS1.

    | Pole | Identifikátor aplikace | popis |
    |---|---|---|
    | ItemId | 01 | Číslo GTIN |

- Na stránce **Zásady GS1** najdete zásadu, jejíž pole **Název zásady** je nastaveno na *Příjem nákupu*. Tato zásada obsahuje následující řádky.

    | Pole | Identifikátor aplikace | popis | Třídění |
    |---|---|---|---|
    | ExpDate | 17 | Datum vypršení platnosti | 0 |
    | InventBatchId | 10 | Číslo dávky | 0 |
    | Množství | 30 | Přijaté množství | 0 |

- Na stránce **Položky nabídky mobilního zařízení** je položka nabídky s názvem *Příjem nákupu*. Její pole **Zásada GS1** je nastaveno na *Příjem nákupu*.

Poté, co zboží pro nákupní objednávku dorazí do skladu, pracovník postupuje podle těchto kroků.

1. V mobilním zařízení vybere položku nabídky **Příjem nákupu**.
1. Zadá číslo nákupní objednávky.
1. Vybere pole **Položka** a naskenuje následující čárový kód: *\]C10100000012345678\~3030\~10b1\~17220215*.

Na základě nastavení, která jsou pro tento příklad vytvořena, systém analyzuje naskenovaný čárový kód následujícím způsobem.

| ID pole | ID aplikace | Hodnota | Poznámka |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Protože pracovník skenoval údaj do pole **Položka**, je do tohoto pole namapována první hodnota v čárovém kódu. Mapování je převzato z obecného nastavení GS1. |
| Množství | 30 | 30 | Protože je v jednom skenování zachyceno několik hodnot polí, toto mapování a všechna zbývající mapování jsou převzata ze zásady GS1, která je přiřazena položce nabídky **Příjem nákupu**. Tato hodnota je množstvím, které bylo přijato. |
| InventBatchId | 10 | b1 | Tato hodnota je ID dávky. |
| ExpDate | 17 | 220215 | Formát data je RRMMDD. Proto je datum vypršení platnosti 15. února 2022. |

Účtenka se poté zaregistruje a po jednom skenování se zadají příslušné hodnoty do databáze.
