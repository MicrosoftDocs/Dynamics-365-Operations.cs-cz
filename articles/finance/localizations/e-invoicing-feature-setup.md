---
title: Práce s nastavením funkcí
description: Toto téma poskytuje informace o nastavení funkcí Elektronické fakturace.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41ffc9c7009291a55392e50c5e490d3288d122bc
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371544"
---
# <a name="work-with-feature-setups"></a>Práce s nastavením funkcí

[!include [banner](../includes/banner.md)]

Chcete-li nastavit generování elektronických souborů a další kroky zpracování (například digitální podepisování souborů, jejich odeslání do vládní webové služby a přijetí odpovědi nebo jejich uložení), nastavte kanál zpracování, pravidla použitelnosti a proměnné pro funkce Elektronické fakturace.

Informace nastavení jsou sloučeny do konceptu *nastavení funkce* koncept a lze je vytvářet, mazat nebo upravovat. U dokončených verzí funkcí Elektronické fakturace lze informace také zobrazit.

Můžete vytvořit tolik položek nastavení funkcí, kolik potřebujete k definování různých scénářů pro generování, zpracování a přijímání elektronických souborů. Přestože tyto položky nastavení funkcí mají nezávislé akce zpracování a podmínky pro provádění, jsou vytvářeny jako součást jediné funkce Elektronické fakturace a dědí její životní cyklus a proces nasazení.

## <a name="add-a-feature-setup"></a>Přidání nastavení funkce

1. Přihlaste se ke svému účtu Regulatory Configuration Service (RCS).
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **Elektronická fakturace**.
3. Na stránce **Funkce Elektronické fakturace** vyberte verzi funkce Elektronické fakturace, která má stav **Koncept**.
4. Na kartě **Nastavení** vyberte **Přidat**.
5. V rozevíracím dialogovém okně **Vytvořit nastavení funkce** ve skupině polí **Nové** vyberte jednu z následujících možností.
 
    - **Vlastní nastavení** – Vytvořte nové nastavení funkce, které má prázdné kanály, prázdný seznam kanálů zpracování, prázdnou sekci pro pravidla použitelnosti a výchozí sadu proměnných v závislosti na typu nastavení.
    - **Z nastavení funkce** – Vytvořte kopii nastavení jiné funkce v rozsahu aktuální funkce Elektronické fakturace.

6. Pokud jste v posledním kroku vybrali možnost **Vlastní nastavení**, zadejte název a popis položky nastavení funkce a poté ve skupině polí **Typ nastavení** vyberte jednu z následujících možností:

    - **Kanál zpracování** – Tuto možnost vyberte, chcete-li generovat a zpracovávat odchozí elektronické dokumenty. U tohoto typu nastavení systém vytvoří prázdný seznam kanálů zpracování, prázdnou sekci pro pravidla použitelnosti a výchozí sadu proměnných. Nebudete moci pracovat s kanály pro příchozí elektronické dokumenty.
    - **Datový kanál** – Tuto možnost vyberte, chcete-li nastavit proces přijímání příchozích elektronických dokumentů z jednoho z definovaných kanálů a jejich předávání přímo do Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management bez dalších akcí. U tohoto typu nastavení systém vytvoří předem definovaný seznam parametrů pro datové kanály, prázdnou sekci pro pravidla použitelnosti a sadu výchozích proměnných. Do kanálu zpracování nebudete moci přidávat žádné akce.
    - **Datový kanál a kanál zpracování** – Tento typ nastavení se podobá typu **Datový kanál**. Než je však příchozí elektronický dokument předán do aplikace Finance nebo Supply Chain Management, můžete nastavit další akce v kanálu zpracování.

7. Pokud jste v posledním kroku vybrali možnost **Datový kanál** nebo **Datový kanál a kanál zpracování**, v poli **Vyberte datový kanál** musíte vybrat kanál, se kterým se chcete integrovat.
8. Vyberte **Vytvořit**.

Po vytvoření nastavení funkce můžete příkazem **Upravit** zahájit jeho konfiguraci.

## <a name="edit-a-feature-setup"></a>Úprava nastavení funkce

V závislosti na typu nastavení funkce můžete konfigurovat proces generování odchozích elektronických souborů a jejich odesílání do externích kanálů, nebo přijímání příchozích dokumentů a jejich předávání do vaší aplikace Finance nebo Supply Chain Management.

### <a name="data-channel"></a>Datový kanál

*Datový kanál* převezme elektronický soubor a buď jej zpracuje, nebo předá přímo do aplikace Finance nebo Supply Chain Management. Tato možnost není dostupná u nastavení funkce typu **Kanál zpracování**.

Chcete-li nastavit datový kanál, zadejte název kanálu. Poté definujte parametry na základě zvoleného typu kanálu. Identifikátor datového kanálu musí odkazovat na proměnnou, která je vytvořena speciálně k identifikaci datového kanálu. Bude použit jako reference v aplikaci Finance nebo Supply Chain Management.

Na kartě **Filtr příloh** měli byste definovat sadu filtrů pro získání konkrétních souborů z kanálu. Můžete vytvořit několik řádků, pokud očekáváte, že soubory budou mít různé přípony názvů souborů nebo pokud musí být soubory zpracovány odlišně v závislosti na názvu souboru. Zde jsou hlavní parametry:

- **Název** – Zadejte název souboru, na který bude systém odkazovat během zpracování. V aplikacích Finance a Supply Chain Management uvidíte soubory v protokolu odeslání.
- **Filtr** – Definujte filtr pro výběr souborů.
- **Volitelné** – Pokud toto políčko není zaškrtnuto, je soubor vyžadován. V tomto případě systém zobrazí chybovou zprávu, pokud kanály neobsahují soubory odpovídající filtru. Tento parametr platí pro e-maily.

Pokud je kanálem poštovní schránka a příchozí e-mail obsahuje několik příloh, můžete konfigurovat pravidla, která definují, jak má služba s přílohami zacházet. Služba může každou přílohu považovat za samostatnou elektronickou fakturu, nebo může jednu přílohu považovat za hlavní fakturu a všechny ostatní přílohy za dodatky.

### <a name="processing-pipeline"></a>Kanál zpracování

*Kanál zpracování* je sada *akcí*, které se spouštějí postupně, dokud nejsou úspěšně dokončeny. Kanál zpracování můžete použít k nastavení procesu pro generování elektronických souborů a provádění dalších kroků (například digitální podepisování souborů, jejich odeslání do externích webových služeb a analýzu odpovědi a příjem a zpracování příchozích dokumentů).

Seznam akcí je předdefinován. Pomocí tlačítek **Nový** a **Odstranit** můžete určit kombinaci akcí, která logicky definuje požadovaný proces pro odesílání nebo přijímání dokumentů.

Pořadí akcí je velmi důležité. Pořadí můžete upravit pomocí tlačítek **Nahoru** a **Dolů**.

Každá akce má sadu parametrů, které můžete konfigurovat nebo upravit. Konkrétní sada parametrů závisí na typu akce.

- **Akce** – Vyberte typ akce.
- **Název akce** - Zadejte název akce. Tento název se objeví v protokolech odeslání a ve zprávách v aplikacích Finance a Supply Chain Management.
- **Popis** – Uveďte více podrobností o účelu akce v procesu.
- **Povolit opakování** – Pokud zaškrtnete toto políčko, můžete vybrat akci v poli **Opakovat akci** a konfigurovat další parametry na kartě **Parametry opakování**.

    Funkce opakování vám umožňuje konfigurovat chování služby, pokud nelze spustit konkrétní akci. Pokud například externí webová služba, ke které se pokoušíte připojit, nereaguje, můžete určit, kolikrát se má systém znovu pokusit o připojení, v jakém intervalu a od jaké akce v kanálu zpracování.

- **Export výsledků** – Toto políčko můžete zaškrtnout pro *jednu* akci v kanálu zpracování. Elektronický soubor, který akce vytvoří v aplikaci Finance nebo Supply Chain Management, lze poté exportovat na stránce **Protokol odeslání elektronických dokumentů**.

### <a name="applicability-rules"></a>Pravidla použitelnosti

*Pravidla použitelnosti* jsou konfigurovatelné klauzule, které poskytují kontext pro spuštění funkcí Elektronické fakturace prostřednictvím sady schopností Elektronické fakturace.
Obchodní dokumenty odesílané z aplikace Finance nebo Supply Chain Management do Elektronické fakturace neobsahují výslovnou referenci, která umožňuje sadě schopností Elektronické fakturace volat konkrétní verzi funkce Elektronické fakturace a konkrétní položku nastavení funkce pro zpracování odeslání. Pokud je však obchodní dokument správně konfigurován, obsahuje povinné prvky, které umožňují Elektronické fakturaci vyřešit, která verze funkce Elektronické fakturace a kanál zpracování musí být vybrán a spuštěn.

Pravidla použitelnosti umožňují službě Elektronické fakturace najít přesné funkce Elektronické fakturace, které je nutné použít ke zpracování podání. Pro vyhledání správných funkcí jsou pole **Kontext** z odeslaného obchodního dokumentu jsou spárována s klauzulemi z pravidel použitelnosti.

S pravidly použitelnosti můžete pracovat následujícími způsoby:

- Výběrem možnosti **Nová** přidáte novou klauzuli do sady pravidel použitelnosti.
- Výběrem příkazu **Odstranit** klauzuli smažete.
- Vyberte několik záznamů a použijte tlačítko **Skupina** nebo **Zrušit seskupení** k vytvoření kombinace položek nebo logických příkazů. Vyberte například řádky, které chcete seskupit, a pak vyberte **Seskupit klauzuli**. Když jsou klauzule seskupeny, je do mřížky přidán nový sloupec. Tento sloupec určuje logický operátor pro seskupenou klauzuli. V současné době jsou podporovány následující typy operátorů:

    - Equal
    - Not equal
    - Větší než / Méně než
    - Větší než nebo rovno / menší nebo rovno
    - Contains
    - Začíná na

    > [!NOTE]
    > Když rušíte seskupení klauzuli, vždy začněte od nejvnitřnější úrovně seskupení.

### <a name="variables"></a>Proměnné

*Proměnné* vám poskytnou větší flexibilitu při nastavování kanálu zpracování a toku dat mezi akcemi. Pro dočasné uložení dat nebo elektronických souborů můžete v některých parametrech akce odkazovat na proměnnou. Některé proměnné se používají k předávání dat mezi aplikacemi Finance nebo Supply Chain Management a službou Elektronická fakturace.

Systém standardně některé proměnné vytvoří sám. Například proměnná **BusinessDocumentDataModel** obsahuje obchodní data ve struktuře JavaScript Object Notation (JSON), která je doručena ve volání z připojené aplikace během procesu odesílání.

K dispozici jsou následující typy proměnných:

- **Konstanta** – Kontejner pro ukládání dočasných dat, která se používají při zpracování akcí kanálu.
- **Od klienta** – Obsah proměnné se získává z klienta Dynamics 365 během spuštění procesu odesílání.
- **Klientovi** – Obsah proměnné je zpřistupněn pro import klientem Dynamics 365 během spuštění procesu odesílání.
- **Datový typ** – Vyberte datový typ informací, které jsou uloženy v proměnné.

### <a name="parameters"></a>Parametry

Možnost **Zakázat redukci obchodních dat** se používá k optimalizaci struktury datové části obchodních dat, která je doručena z aplikace Finance nebo Supply Chain Management během elektronického odesílání dokumentů. Optimalizace pomáhá redukovat data, která směřují do služby Elektronická fakturace za účelem další transformace do požadovaného elektronického souboru. Výchozí hodnota je **Ne**.

- **Ano** – Aplikace Finance nebo Supply Chain Management odešle soubor JSON struktury **Model faktury** nebo **Fiskální model** (pro Brazílii), která je definována v modulu **Elektronické hlášení**. Všechny prvky modelu jsou na straně aplikace naplněny obchodními daty bez ohledu na konečnou strukturu elektronického souboru. Modely obvykle obsahují více obchodních dat, než vyžaduje struktura cílového souboru, a generování těchto dat v aplikaci může vyžadovat více času. Hodnota **Ano** je u této možnosti vyžadována ve vzácných případech, kdy chcete generovat různé výstupní soubory v jedné funkci elektronické fakturace a nastavení funkce. Hodnota **Ano** je užitečná při odstraňování problémů se scénáři, strukturou elektronických souborů a úplností obchodních dat.
- **Ne** – Aplikace Finance nebo Supply Chain Management provede první volání služby bez jakýchkoli obchodních dat. Účelem této výzvy je získat informace o konfiguraci elektronického hlášení (ER), která bude použita pro transformaci elektronického souboru v kanálu zpracování. Tyto informace se vrátí do aplikace, která je použije k určení podmnožiny obchodních dat, která by měla být zahrnuta v souboru JSON struktury **Model faktury** nebo **Fiskální model** (pro Brazílii). Hodnota **Ne** u této možnosti pomáhá snížit objem obchodních dat, které aplikace odesílá do služby, protože aplikace může odeslat pouze obchodní data, která jsou nezbytná pro úspěšné vygenerování elektronického souboru.

### <a name="validate-a-feature-setup"></a>Ověření nastavení funkce

Spuštěním ověření zkontrolujete konzistenci celé konfigurace. Například, pokud je povinný parametr akce ponechán prázdný, ověření zjistí tuto nekonzistenci a zobrazí se varování.

- Na stránce **Nastavení verze funkce** v podokně akcí vyberte **Ověřit**.

## <a name="delete-a-feature-setup"></a>Odstranění nastavení funkce

1. Na stránce **Funkce Elektronické fakturace** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.
2. Na kartě **Nastavení** vyberte **Odstranit**.
3. V okně se zprávou, které se zobrazí, výběrem tlačítka **Ano** potvrďte, že chcete odstranit nastavení funkce.
