---
title: Flexibilní zásada rezervace dimenze na úrovni skladu
description: V tomto tématu jsou popsány zásady rezervace zásob, které umožňují společnostem prodávat produkty sledované podle dávky a spustit jejich logistiku, protože operace s povoleným WMS rezervují konkrétní dávky pro prodejní objednávky zákazníka, a to i v případě, že hierarchie rezervací, přidružená k produktům, neumožňuje rezervaci specifických dávek.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec80346126713cc604b00e6ca7f6e8f4c242dc6f
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530298"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Flexibilní zásada rezervace dimenze na úrovni skladu

[!include [banner](../includes/banner.md)]

Pokud je hierarchie rezervací zásob typu Batch-below\[location\] spojena s produkty, podniky, které prodávají produkty sledované podle dávky a spouštějí své logistiku jako operace, které jsou povoleny pro Microsoft Dynamics 365 Warehouse Management System (WMS), nemohou rezervovat konkrétní dávky těchto produktů pro prodejní objednávky odběratele. V tomto tématu jsou popsány zásady rezervace zásob, které těmto podnikům umožňují rezervovat specifické dávky, a to i v případě, že jsou produkty přiřazeny k hierarchii rezervací Batch-below\[location\].

## <a name="inventory-reservation-hierarchy"></a>Hierarchie rezervací zásob

V tomto oddílu je shrnuta existující hierarchie rezervací zásob. Zaměřuje se na způsob, jakým je nakládáno s položkami sledovanými dávkou a sériovým číslem.

Hierarchie rezervace zásob určuje, že pokud se jedná o dimenze uskladnění, objednávka poptávky nese povinné dimenze pracoviště, skladu a stavu zásob, zatímco logika skladu je odpovědná za přiřazení skladového místa k požadovanému množství a rezervaci skladového místa. Jinak řečeno, v interakcích mezi objednávkou poptávky a skladovými operacemi se očekává, že objednávka poptávky indikuje, odkud musí být objednávka expedována (tj. pracoviště a sklad). Sklad pak spoléhá na svou logiku k nalezení požadovaného množství v skladových prostorách.

Chcete-li však zohlednit provozní model podniku, je sledovací dimenze (dávka a sériová čísla) předmětem větší flexibility. Hierarchie rezervací zásob může vyhovovat situacím, pro které platí následující podmínky:

- Podnik spoléhá na své skladové operace za účelem správy výdeje množství, která mají čísla dávek nebo sériová čísla po nalezení množství v prostoru úložiště skladu. Tento model se často označuje jako *Batch-below\[location\]*. Obvykle se používá v případě, že identifikace dávky nebo sériového čísla produktu není důležitá pro zákazníky, kteří učiní poptávku u prodávající společnosti.
- Pokud jsou dávka a sériová čísla součástí specifikace objednávky odběratele a jsou zaznamenána na objednávce poptávky, skladové operace, které vyhledají množství ve skladu, jsou omezeny konkrétními požadovanými počty a nejsou povoleny jejich změny. Tento model se označuje jako *Batch-above\[location\]*.

V těchto scénářích je výzvou, že každému uvolněnému produktu lze přiřadit pouze jednu hierarchii rezervace zásob. Proto, aby WMS zpracoval sledované položky, poté, co v přiřazení hierarchie určí, kdy má být provedena rezervace dávky nebo sériového čísla (buď při objednávce poptávky nebo při zahájení práce výdeje skladu), toto časování nelze změnit ad hoc.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Pružná rezervace pro položky sledované dávkou

### <a name="business-scenario"></a>Scénáře obchodu

V tomto scénáři společnost používá strategii zásob, při které je dokončené zboží sledováno pomocí čísel dávek. Tato společnost také používá pracovní vytížení WMS. Vzhledem k tomu, že toto pracovní vytížení má dobře vybavenou logiku pro plánování a provádění operací výdeje a expedice skladu pro položky s povolenou dávkou, je většina dokončených položek přidružena k hierarchii rezervací zásob "Batch-below\[location\]". Výhodou tohoto typu operačního nastavení je to, že rozhodnutí (což jsou ve skutečnosti rozhodnutí o rezervacích) o tom, které dávky vyskladnit a do jakého skladu je vložit, budou odloženy až do zahájení operace výdeje skladu. Nejsou provedeny při učinění objednávky odběratele.

Ačkoliv hierarchie rezervací Batch-below\[location\] slouží k zajištění správných obchodních cílů společnosti, mnoho zavedených zákazníků společnosti vyžaduje stejnou dávku, při které byly tyto produkty zakoupeny dříve. Z toho vyplývá, že společnost hledá flexibilitu ve způsobu, jakým jsou zpracovávána pravidla rezervace dávky, takže v závislosti na poptávce odběratelů po stejné položce dojde k následujícímu chování:

- Číslo dávky lze zaznamenat a rezervovat, když je objednávka provedena, zpracovatelem prodeje, a nelze ji změnit během skladových operací anebo pořídit jinými požadavky. Toto chování pomáhá zaručit, že objednané číslo dávky je expedováno odběrateli.
- Není-li číslo dávky pro odběratele důležité, skladové operace mohou určit číslo dávky během výdejní práce po provedení registrace prodejní objednávky a rezervace.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Povolení rezervace konkrétní dávky v prodejní objednávce

Chcete-li přizpůsobit požadovanou flexibilitu v chování rezervace dávek u položek, které jsou přidruženy k hierarchii rezervace zásob Batch-below\[location\], musí manažeři zásob zaškrtnout políčko **Povolit rezervaci na objednávce poptávky** pro úroveň **čísla dávky** na stránce **hierarchie rezervací zásob**.

![Zflexibilnění hierarchie rezervace zásob](media/Flexible-inventory-reservation-hierarchy.png)

Je- li vybrána úroveň **čísla dávky** v hierarchii, budou automaticky vybrány všechny dimenze nad úrovní a až k úrovni **skladového místa**. (Ve výchozím nastavení jsou přednastaveny všechny dimenze nad úrovní **skladového místa**.) Toto chování odpovídá logice, kde jsou všechny dimenze v rozsahu mezi číslem dávky a místem automaticky rezervovány po rezervaci konkrétního čísla dávky na řádku objednávky.

> [!NOTE]
> Zaškrtávací políčko **Povolit rezervaci na objednávce poptávky** se vztahuje pouze na úrovně hierarchie rezervací, které jsou pod dimenzí skladového místa.
>
> **Číslo dávky** je jediná úroveň v hierarchii, která je otevřená pro zásadu pružné rezervace. Jinými slovy, pro úroveň **umístění**, **registrační značky** nebo **sériového čísla** nelze zaškrtnout políčko **Povolit rezervaci na objednávce poptávky**.
>
> Pokud hierarchie rezervace obsahuje dimenzi sériového čísla (která musí vždy být nižší než úroveň **Číslo dávky**) a pokud jste pro číslo dávky aktivovali rezervaci specifickou pro dávku, systém bude pokračovat ve zpracování rezervací sériových čísel a operací výdeje na základě pravidel, která platí pro zásadu rezervace Serial-below\[location\].

V kterémkoli bodě můžete povolit rezervaci specifickou pro dávku pro existující hierarchii rezervací Batch-below\[location\] v rámci vašeho nasazení. Tato změna neovlivní žádné rezervace a otevřené práce skladu, které byly vytvořeny před provedením změny. Zaškrtnutí políčka **Povolit rezervaci na objednávce poptávky** však nelze odstranit, pokud pro jednu nebo více položek které jsou přidruženy k dané hierarchii rezervací, existují transakce zásob typů výdeje **Rezervované objednané**, **Rezervované – fyzicky**, nebo **Objednáno**.

> [!NOTE]
> Pokud existující hierarchie rezervací položky nepovoluje dávkovou specifikaci pro objednávku, můžete ji přiřadit k hierarchii rezervací, která povoluje specifikaci dávky, pokud je struktura úrovně hierarchie v obou hierarchiích stejná. Použijte funkci **Změnit hierarchii rezervací pro položky** pro provedení opětovného přiřazení. Tato změna může být důležitá v případě, že chcete zabránit flexibilní rezervaci dávky pro podmnožinu položek sledovaných dávkou, ale povolit ji pro zbytek portfolia produktů.

Bez ohledu na to, zda jste zaškrtli políčko **Povolit rezervaci na objednávce poptávky**, nechcete-li rezervovat určité číslo dávky pro položku na řádku objednávky, bude stále platit výchozí logika skladového místa, která je platná pro hierarchii rezervace Batch-below\[location\].

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Rezervace konkrétního čísla dávky pro objednávku odběratele

Po nastavení hierarchie rezervací zásob Batch-below\[location\] pro položku sledovanou dávkou za účelem umožnění rezervace konkrétních čísel dávky na prodejních objednávkách mohou zpracovatelé prodejní objednávky provést objednávky odběratele pro stejnou položku jedním z následujících způsobů:

- **Zadat podrobnosti objednávky bez zadání čísla dávky** – tento přístup by měl být použit v případě, že specifikace dávky produktu není pro odběratele důležitá. Všechny existující procesy související se zpracováním objednávky tohoto typu v systému zůstanou nezměněny. Na straně uživatelů nejsou vyžadovány žádné další úvahy.
- **Zadat podrobnosti objednávky a rezervovat určité číslo dávky** – tento přístup by měl být použit v případě, že odběratel požaduje určitou dávku. Zákazníci obvykle požadují určitou dávku při opětovném objednání produktu, který dříve nakoupili. Tento typ rezervace specifické pro dávku se nazývá *rezervace potvrzená objednávkou*.

Následující sada pravidel je platná při zpracování množství a číslo dávky je potvrzeno pro specifickou objednávku:

- Chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa. Tento rozsah obvykle zahrnuje dimenzi registrační značky.
- Směrnice skladových míst se nepoužívají, pokud je pro řádek prodeje vytvořena výdejní práce, která používá rezervaci dávky potvrzenou objednávkou.
- Během zpracování práce skladu pro dávky potvrzené objednávkou nemůže uživatel ani systém změnit číslo dávky. (Toto zpracování zahrnuje zpracování výjimek.)

Následující příklad ukazuje celý tok.

## <a name="example-scenario"></a>Příklad

Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Nastavení hierarchie rezervací zásob, aby byla povolena rezervace specifická pro dávku

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Zásoby \> Hierarchie rezervací**.
2. Zvolte **Nové**.
3. Do pole **Název** zadejte název (například **BatchFlex**).
4. Do pole **Popis** zadejte popis (například **Batch below flexible**).
5. V poli **Vybrané** zvolte **Sériové číslo** a **Vlastník** a poté zvolte tlačítko šipky doleva pro přesun na pole **K dipozici**.
6. Vyberte **OK**.
7. V řádku pro úroveň dimenze **Číslo dávky** zaškrtněte políčko **Povolit rezervaci na objednávce poptávky**. Úrovně **Registrační značka** a **Skladové místo** jsou vybrány automaticky a nelze u nich zrušit zaškrtávací políčko.
8. Zvolte **Uložit**.

### <a name="create-a-new-released-product"></a>Vytvoření nového uvolněného produktu

1. Pomocí těchto hodnot nastavíte tři základní datové parametry produktu:

    - V poli **Skupina dimenze úložiště** vyberte **Ware**.
    - V poli **Skupina sledovací dimenze** vyberte **Batch-Phy**.
    - V poli **Hierarchie rezervace** vyberte **BatchFlex**.

2. Vytvořte dvě čísla dávek, jako například **B11** a **B22**.
3. Přidejte množství položek k zásobám na skladě pomocí následujících hodnot.

    | Sklad | Číslo dávky | Umístění | Poznávací značka | Množství |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Žádní          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Zadání podrobností prodejní objednávky

1. Přejděte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. V záhlaví prodejní objednávky v poli **Účet odběratele** zadejte **US-003**.
4. Přidejte řádek pro novou položku a jako množství zadejte **10**. Ujistěte se, že je v poli **Sklad** nastavena hodnota na **24**.
5. Na záložce s náhledem **Řádky prodejní objednávky** vyberte možnost **Zásoby** a poté ve skupině **Udržovat** vyberte možnost **Rezervace dávky**. Stránka **Rezervace dávky** zobrazí seznam dávek, které jsou k dispozici pro rezervaci pro daný řádek objednávky. V tomto příkladu se zobrazí množství **20** pro číslo dávky **B11** a množství **10** pro číslo dávky **B22**. Všimněte si, ke stránce **Rezervace dávky** nelze získat přístup z řádku, pokud je položka na tomto řádku přidružena k hierarchii rezervace Batch-below\[location\] v případě, že není nastavena tak, aby umožňovala rezervaci specifickou pro dávku.

    > [!NOTE]
    > Chcete-li rezervovat určitou dávku pro prodejní objednávku, je nutné použít stránku **Rezervace dávky**.
    >
    > Zadáte-li číslo dávky přímo do řádku prodejní objednávky, systém se bude chovat, jako byste zadali konkrétní hodnotu dávky pro položku, na kterou se vztahuje zásada rezervace Batch-below\[location\]. Po uložení řádku se zobrazí varovná zpráva. Pokud potvrdíte, že číslo dávky by mělo být zadáno přímo na řádku objednávky, řádek nebude zpracován běžnou logikou správy skladu.
    >
    > Pokud rezervujete množství na stránce **Rezervace**, žádná specifická dávka nebude rezervována a provedení skladových operací pro tento řádek bude následovat pravidla aplikovatelná pod zásadami rezervace Batch-below\[location\].

    Tato stránka obecně funguje a je v interakci stejným způsobem, jako pracuje a je závislá na položkách, které mají přidruženou hierarchii rezervací typu Batch-above\[location\]. Platí však následující výjimky:

    - Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** zobrazí čísla dávek, která jsou vyhrazena pro řádek objednávky. Hodnoty dávky v mřížce se zobrazí v průběhu cyklu realizace řádku objednávky včetně fází zpracování skladu. Naopak na záložce s náhledem **Přehled** je běžná rezervace řádku objednávky (tj. rezervace, která se provádí pro dimenze nad úrovní **skladového místa**), v mřížce zobrazena až do bodu vytvoření skladové práce. Entita práce pak převezme rezervaci řádku a na stránce se již nebude zobrazovat rezervace řádku. Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** pomáhá zajistit, že procesor prodejní objednávky může zobrazit čísla dávek, která byla potvrzena do objednávky zákazníka v kterémkoli okamžiku během svého životního cyklu, až do fakturace.
    - Kromě rezervace konkrétní dávky může uživatel ručně vybrat konkrétní místo dávky a registrační značku namísto toho, aby je systém vybral automaticky. Tato schopnost souvisí s návrhem mechanismu rezervace dávky potvrzené objednávkou. Jak bylo zmíněno dříve, chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa. Skladová práce proto bude mít stejné dimenze uskladnění, které byly rezervovány uživateli, kteří pracovali s objednávkami, a nemusí vždy představovat umístění úložiště položek, které je pro operace výdeje vhodné nebo dokonce možné. Pokud zpracovatelé objednávek vědí o omezeních skladu, mohou chtít ručně vybrat určitá skladová místa a registrační značky při rezervaci dávky. V takovém případě musí uživatel použít funkci **Zobrazit dimenze** v záhlaví stránky a přidat umístění a registrační značku do mřížky na záložce s náhledem **Přehled**.

6. Na stránce **Rezervace dávky** vyberte řádek pro dávku **B11** a pak vyberte **Řádek rezervace**. V průběhu automatické rezervace není určena žádná logika pro přiřazování skladových míst a registračních značek. Množství lze ručně zadat do pole **Rezervace**. Všimněte si, že na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** se zobrazí dávka **B11** jako **Potvrzená**.

    ![Potvrzení konkrétního čísla dávky na řádek prodejní objednávky na stránce rezervace dávky](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Rezervaci množství na řádku prodejní objednávky lze provést ve více dávkách. Stejně tak lze provést rezervaci stejné dávky proti několika místům a registračním značkám (pokud jsou pro skladová místa povoleny registrační značky).
    >
    > Rezervace konkrétní dávky pro množství na řádku prodejní objednávky může být také částečná. Například celkové množství 100 jednotek může být rezervováno tak, aby určitá dávka byla potvrzena na 20 jednotek, zatímco 80 jednotek je rezervováno na pracovišti a na úrovni skladů pro všechny dostupné dávky. V tomto případě bude WMS zpracovávat operace výdeje pomocí dvou oddělených řádků práce.

7. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**. Vyberte položku a poté vyberte **Spravovat zásoby** \> **Zobrazení** \> **Transakce**.

    ![Rezervace potvrzená objednávkou jako typ skladové transakce](media/Inventory-transactions-for-order-committed-reservation.png)

8. Zkontrolujte skladové transakce položky, které souvisejí s rezervací řádku prodejní objednávky.

    - Transakce, ve které je pole **Odkaz** nastaveno na **Prodejní objednávka** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro dimenze zásob nad úrovní **skladového místa**. Podle hierarchie rezervací zásob položky jsou tyto dimenze pracoviště, sklad a stav zásob.
    - Transakce, ve které je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro specifickou dávku a pro všechny dimenze zásob nad ní. Podle hierarchie rezervací zásob položky jsou tyto dimenze číslo dávky a skladové místo. V tomto příkladu je skladové místo **Bulk-001**.

9. V záhlaví prodejní objednávky vyberte **Sklad** \> **Akce** \> **Uvolnění do skladu**. Řádek objednávky je nyní ve vlně a vytvoří se vytížení a práce.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Kontrola a zpracování práci skladu s čísly dávek potvrzených objednávkou

1. Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad** \> **Podrobnosti práce**.

    Práce, která zpracovává operaci výdeje pro množství dávky potvrzené v řádku prodejní objednávky, má následující charakteristiky:

    - Chcete-li vytvořit práci, systém použije šablony práce, ale ne směrnice skladového místa. Chcete-li určit, kdy má být vytvořena nová práce, bude použito standardní nastavení definované pro šablony práce, jako je například maximální počet řádků výdeje nebo určitá měrná jednotka. Pravidla, která jsou spojena se směrnicemi skladových míst pro určení skladových místa výdeje, však nejsou zvažována, protože rezervace potvrzená objednávkou již určuje všechny dimenze zásob. Tyto dimenze zásob obsahují dimenze na úrovni skladového místa. Tato práce tedy tyto dimenze zdědí bez nutnosti konzultovat směrnice skladového místa.
    - Číslo dávky není zobrazeno na řádku výdeje (jako je například případ pro řádek práce vytvořený pro položku, která má přidruženou hierarchii rezervace Batch-above\[location\].) Místo toho se v poli "od" číslo dávky a všechny ostatní dimenze uskladnění zobrazí na skladové transakci řádku práce, která je odkazována z přidružených skladových transakcí.

        ![Skladová transakce pro práci, která pochází z rezervace potvrzené objednávkou](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Po vytvoření práce se skladová transakce položky, kde je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou**, odstraní. Skladová transakce, kde je pole **Odkaz** nastaveno na **Práce**, nyní ukládá fyzickou rezervaci ve všech dimenzích zásob.

        Skladové operace mohou pokračovat v provádění práce obvyklým způsobem. Pokyny v mobilním zařízení však nařídí pracovníkovi, aby vydával určité číslo dávky. V prostředích skladu, kde jsou skladová místa řízena registrační značkou, poté, co pracovník dostane do skladového místa, kde je uložena stejná dávka na více registračních štítků, může vybírat z libovolné registrační značky, která ještě není rezervována (například jinou rezervace nebo práce potvrzené objednávkou, která pochází z rezervace daného typu.)

        Pokud z místa uvedeného na řádku práce odcházíte k vyskladnění, mohou operátoři skladu použít jednu z následujících akcí, které přesměrují výběr konkrétní dávky z vhodnějšího umístění:

        - Standardní akce **Přepsat umístění** na mobilním zařízení (za předpokladu, že je nastavení **Umožnit přepis výdejního umístění** pracovníka skladu povoleno)
        - Akce **Změnit umístění** na stránce **Podrobnosti seznamu práce**. 

2. V mobilním zařízení dokončete výdej a vklad práce.

    Množství **10** pro číslo dávky **B11** je nyní vyskladněno pro řádek prodejní objednávky a je vloženo do umístění **Portál**. V tomto okamžiku je vše připraveno k naložení na nákladní vůz a odesláno na adresu odběratele.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Zpracování výjimky práce skladu s čísly dávek potvrzených objednávkou

Práce na skladě pro výdej čísel dávek potvrzených objednávkou podléhá stejnému standardnímu zpracování výjimek a akcím při běžné práci. Obecně platí, že otevřenou práci nebo řádek práce lze zrušit, lze je přerušit, protože skladovací místo uživatele je plné, může být krátkodobě vyskladněno a je aktualizovat z důvodu přesunu. Stejně tak lze snížit vyskladněné množství práce, které již bylo dokončeno, nebo lze stornovat práci.

Následující pravidlo klíče se použije na všechny tyto akce zpracování výjimek: číslo dávky, které bylo rezervováno pro odběratele, nelze nikdy nahradit jiným číslem dávky, ale dimenze uskladnění (umístění a registrační značka) mohou být změněny buď pomocí Ruční aktualizace uživatelem nebo automatickou aktualizací systémem. Automatická aktualizace je založena na stejném náhodném přiřazení dimenzí úložiště, které byly použity, když byla určitá dávka automaticky rezervována, ale nebyly zadány žádné dimenze úložiště.

### <a name="example-scenario"></a>Příklad

Příkladem tohoto scénáře je situace, kdy je dříve dokončená práce vyzvednuta pomocí funkce **Snížit vyskladněné množství**. Tento příklad pokračuje v předchozím příkladu v tomto tématu.

1. Přejděte na **Řízení skladu** \> **Nakládky** \> **Aktivní nakládky**.
2. Vyberte nakládku, která byla vytvořena v souvislosti s dodávkou prodejní objednávky.
3. Na záložce s náhledem **Naložit řádky objednávky** zvolte **Snížit vyskladněné množství**.
4. Na stránce **Snížit vyskladněné množství** vyberte v poli **Přesunout na místo** možnost **FL-001**.
5. V poli **Přejít na registrační značku** zvolte **LP33**.
6. V mřížce v poli **Skladové množství ke zrušení výdeje** zadejte **10**.
7. Vyberte **OK**.

Zde jsou výsledky akce zrušení výdeje:

- Stav dříve uzavřené práce je nastaven na **Zrušeno**.
- Nová práce typu **Přesun zásob** se vytvoří pro nevyzvednuté množství **10** pro číslo dávky **B11**. Tato práce představuje přesun z místa **Portál** na registrační značku **LP33** v umístění **FL-001**. Stav je nastaven na **Zavřeno**.
- Systém znovu rezervuje číslo dávky, které bylo původně objednáno, a přiřadí ID umístění a registrační značky. (Tento proces odpovídá spuštění funkce **Rezervovat řádek** pro řádek objednávky pro dané číslo dávky). Výsledkem je, že se dávka **B11** zobrazí jako potvrzená na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** na stránce **Rezervace dávky**, a pole **Rezervace** obsahuje množství **10** pro číslo dávky **B11**. Dále je pole **Místo** nastaveno na **FL-001** a pole **Registrační značka** je nastaveno na **LP11**. (Tato pole můžete přidat do mřížky, pokud nejsou viditelná.)

V následujících tabulkách je uveden přehled, který zobrazuje způsob, jakým systém zpracovává rezervace dávky potvrzené objednávkou pro určité akce skladu. Chcete-li interpretovat obsah v tabulkách, předpokládejme, že každá akce skladu je spuštěna v kontextu existující práce ve skladu, která pochází z rezervace dávky potvrzené objednávkou, nebo že provádění jednotlivých akcí skladu ovlivňuje práci tohoto typu.

> [!NOTE]
> V těchto tabulkách sloupec "množství dávky je k dispozici" označuje, zda množství dávky k dispozici kromě množství, které již bylo rezervováno pro aktuální potvrzené rezervace nebo již rezervované pro práci ve skladu pochází z rezervací daného typu.

#### <a name="override-the-pick-location-on-the-open-work"></a>Přepsání místa výdeje na otevřené práci

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Možnost <strong>Umožnit přepis výdejního umístění</strong> je povolena na pracovníkovi.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Přepsat umístění</strong> v aplikaci skladu při zahájení práce výdeje.</li>
<li>Vyberte <strong>Navrhnout</strong>.</li>
<li>Potvrďte nové skladové místo navrhované na základě dostupnosti množství dávky.</li>
</ol>
</td>
<td>Při aktuální práci dojde k následujícím akcím:
<ul>
<li>Místo na řádku výdeje je aktualizováno na nové místo. (Je-li toto umístění řízeno registrační značkou, je k skladové transakci práce přiřazena náhodná registrační značka a pracovník může vybírat z registračních značek, které mají dostupné množství.)</li>
<li>Pokud se množství nachází na více než jedné registrační značce v novém skladovém místě, bude původní řádek výdeje rozdělen do několika řádků tak, aby souhlasila každá registrační značka.</li>
</ul>
</td>
<td>Nelze použít</td>
</tr>
<tr>
<td>Žádný</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Přepsat umístění</strong> v aplikaci skladu při zahájení práce výdeje.</li>
<li>Zadat ručně místo.</li>
</ol>
</td>
<td>Akce <strong>Přepsání místa</strong> není možná. Dojde k selhání a dojde k vyvolání chyby.</td>
<td>Nelze použít</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Tlačítko Úplné – rozdělení řádku práce z důvodu přetečení v umístění uživatele

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td>Možnost <strong>Povolit rozdělení práce</strong> je povolena na položce nabídky mobilního zařízení.</td>
<td>Nelze použít</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Úplný</strong> v aplikaci skladu při zpracování práce výdeje.</li>
<li>Do pole <strong>Vyskladněné množství</strong> zadejte částečné množství požadovaného výdeje, které označuje plnou kapacitu.</li>
</ol>
</td>
<td>
<ul>
<li>Při aktuální práci je množství aktualizováno na zbývající množství, které musí být vyskladněno.</li>
<li>Nová práce pro vyskladněné množství je vytvořena a uzavřena.</li>
</ul></td>
<td>Nelze použít</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Snížení vyskladněného množství dokončené práce (z nákladu)

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Nelze použít</td>
<td>Ano</td>
<td>
<ol>
<li>Otevřete stránku <strong>Snížit vyskladněné množství</strong> z řádku vytížení.</li>
<li>Zadejte úplné množství pro zrušení výdeje.</li>
<li>Vyberte přesun do místa / na registrační značku.</li>
</ol>
</td>
<td>
<ul> 
<li>Práce, která je přidružená k řádku vytížení, je zrušena.</li>
<li>Nová práce pro přesun zásob je vytvořena a uzavřena.</li>
</ul>
</td>
<td>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Viz předchozí řádek.</td>
<td>Množství je znovu rezervováno pro stejnou dávku a pro stejné skladové místo a registrační značku (jedná-li se o místo řízené registrační značkou), které byly zadány při zrušení výdeje.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Přesunutí položky v rámci skladu

> [!NOTE]
> Tuto akci skladu lze použít pouze pro přesun typu **Proces pro vytvoření práce**, nikoli pro přesun podle šablony.

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Možnost <strong>Povolit pohyb zásob s přidruženou prací</strong> je povolena u pracovníka.</td>
<td>Ano</td>
<td>
<ol>
<li>Zahajte přesun v aplikaci skladu.</li>
<li>Zadejte místa z a do.</li>
</ol></td>
<td>
<ul>
<li>Ve všech existujících pracích, které jsou přesunutím ovlivněny, se skladové místo výdeje aktualizuje na nové umístění "do".</li>
<li>Nová práce pro přesun zásob je vytvořena a uzavřena.</li>
</ul>
</td>
<td>Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, budou znovu rezervovány pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Viz předchozí řádek.</td>
<td>Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, jsou znovu rezervovány pro stejnou dávku a pro nové umístění "do" a registrační značku (pokud je toto umístění řízeno registrační značkou).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Rezervace vyskladněného množství dokončené práce (z nákladu nebo vlny)

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Nelze použít</td>
<td>Ano</td>
<td>
<ol>
<li>Otevřete stránku <strong>Stornovat práci</strong>.</li>
<li>Na stránce s požadavkem vyberte možnost <strong>Ponechat položky v aktuálním umístění</strong>.</li>
</ol>
</td>
<td>Veškerá práce, která je přidružená k řádku vytížení, je zrušena.</td>
<td>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Viz předchozí řádek.</td>
<td>Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kde bylo množství ponecháno při stornování.</td>
</tr>
<tr>
<td>Ano</td>
<td>
<ol>
<li>Otevřete stránku <strong>Stornovat práci</strong>.</li>
<li>Na stránce s požadavkem vyberte možnost <strong>Přiřadit položky k tomuto umístění</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Aktuální práce je zrušena.</li>
<li>Nová práce pro přesun zásob je vytvořena a uzavřena.</li>
</ul>
</td>
<td>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Viz předchozí řádek.</td>
<td>Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kterým bylo množství přiřazeno při stornování.</td>
</tr>
<tr>
<td>Ano/Ne</td>
<td>
<ol>
<li>Otevřete stránku <strong>Stornovat práci</strong>.</li>
<li>Na stránce s požadavkem vyberte možnost <strong>Přesunout položky do tohoto umístění</strong>.</li>
</ol>
</td>
<td>Storno není podporováno.</td>
<td>Nelze použít</td>
</tr>
<tr>
<td>Ano/Ne</td>
<td>
<ol>
<li>Otevřete stránku <strong>Stornovat práci</strong>.</li>
<li>Na stránce s požadavkem vyberte možnost <strong>Přesunout položky podle směrnic skladového umístění</strong>.</li>
</ol>
</td>
<td>Storno není podporováno. </td>
<td>Nelze použít</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Krátkodobý výdej a množství – Zaregistrujte množství jako fyzicky nenalezené nav místě nebo na registrační značce během provádění práce výdeje.

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</li>
<li>Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</li>
<li>Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</li>
</ul>
</td>
<td>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>
<ul>
<li>Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</li>
<li>Aktuální práce zůstane otevřená.</li>
</ul>
</td>
<td>Nelze použít</td>
</tr>
<tr>
<td rowspan='2'>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</li>
<li>Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</li>
<li>Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</li>
</ul>
</td>
<td>Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou znovu rezervovány pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Viz předchozí řádek.</td>
<td>Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou odstraněny.</td>
</tr>
<tr>
<td>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne/Ano</strong>. Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</li>
<li>V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</li>
<li>V seznamu vyberte umístění/registrační značku.</li>
</ol>
</td>
<td>
<ul>
<li>Při aktuální práci dojde k následujícím akcím:
<ul>
<li>Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</li>
<li>Řádek vložení je zrušen.</li>
<li>Je vytvořen nový řádek vyskladnění. Používá se místo / registrační značka, které uživatel vybral.</li>
<li>Je vytvořen nový řádek vložení.</li>
</ul>
</li>
<li>Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</li>
</ul>
</td>
<td>Nelze použít</td>
</tr>
<tr>
<td>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>. Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</td>
<td>Žádný</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</li>
<li>V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</li>
</ol>
</td>
<td>Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</td>
<td>Nelze použít</td>
</tr>
<tr>
<td>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>. Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</td>
<td>Žádný</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</li>
<li>V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</li>
<li>V seznamu vyberte umístění/registrační značku.</li>
</ol>
</td>
<td>
<ul>
<li>Při aktuální práci dojde k následujícím akcím:
<ul>
<li>Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</li>
<li>Řádek vložení je zrušen.</li>
</ul>
</li>
<li>Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</li>
</ul>
</td>
<td>Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě /registrační značce krátkodobého výdeje, budou odstraněny.</td>
</tr>
<tr>
<td>Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Automatický</strong>, <strong>Úprava zásob</strong> = <strong>Ano/Ne</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano/Ne</strong>.</td>
<td>Nelze použít</td>
<td>
<ol>
<li>Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</li>
<li>Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</li>
<li>V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s automaticky opakovaným přidělením</strong>.</li>
</ol>
</td>
<td>Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</td>
<td>Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Změnit stav zásob

> [!NOTE]
> Tuto akci skladu lze provést z více vstupních bodů. Zde zobrazený příklad používá akci **Změna stavu zásob** na stránce **Množství na skladě podle místa**.

<table>
<thead>
<tr>
<th>Klíčové parametry nastavení</th>
<th>Množství dávky je dostupné</th>
<th>Klíčové kroky uživatele</th>
<th>Práce skladu</th>
<th>Rezervace dávky potvrzené objednávkou</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Rezervace</strong> nebo <strong>Označení a rezervace</strong>.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte konkrétní umístění.</li>
<li>Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</li>
<li>Zvolte <strong>Změna stavu zásob</strong>.</li>
<li>Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</li>
</ol>
</td>
<td>Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</td>
<td>
<ul>
<li>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</li>
<li>Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</li>
<li>Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</li>
</ul>
</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</td>
<td>
<ul>
<li>Rezervace je odebrána.</li>
<li>Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</li>
<li>Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Žádná</strong>.</td>
<td>Ano</td>
<td>
<ol>
<li>Vyberte konkrétní umístění.</li>
<li>Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</li>
<li>Zvolte <strong>Změna stavu zásob</strong>.</li>
<li>Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</li>
</ol>
</td>
<td>Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</td>
<td>Množství je znovu rezervováno pro stejnou dávku. Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</td>
</tr>
<tr>
<td>Ne</td>
<td>Viz předchozí řádek.</td>
<td>Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</td>
<td>Změny stavu zásob nejsou povoleny.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Omezení

- Flexibilní funkce rezervace dimenzí na úrovni skladu nepodporuje následující funkce:

    - Správa skutečné hmotnosti
    - Záporný fyzický sklad
    - Rezervace proti objednané dodávce
    - Převodní příkazy a výdej surovin

- Pravidlo konsolidace kontejneru pro balení podle jednotky předpisu má omezení. V případě rezervací potvrzených objednávkou doporučujeme nepoužívat šablony sestavení kontejnerů, kde je povoleno pole **Zabalit podle jednotky přepisu**. V aktuálním návrhu nejsou při vytvoření skladové práce použity směrnice skladového místa. Z tohoto důvodu je při kroku vlny vytváření kontejnerů použita pouze nejnižší jednotka ve skupině klasifikace jednotek (skladová jednotka).
