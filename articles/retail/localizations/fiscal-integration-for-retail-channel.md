---
title: "Fiskální integrace pro maloobchodní síť"
description: "V tomto tématu je uveden přehled fiskální integrace pro Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: cs-cz
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Fiskální integrace pro maloobchodní síť

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled o funkci fiskální integrace, která je k dispozici v aplikaci Microsoft Dynamics 365 for Retail. Funkci fiskální integrace je architektura navržená pro podporu místních daňových předpisů, které mají za cíl zabránit podvodům v oblasti maloobchodu. Typický scénáře, které lze pokrýt pomocí fiskální integrace, zahrnují:

- Tisk fiskální příjemky a její předání odběrateli.
- Zabezpečení odeslání informací týkajících se prodeje a vrácení provedených na POS do externí služby poskytované úřadem.
- Použití ochrany dat pomocí digitálního podpisu autorizovaného úřadem..

Toto téma obsahuje pokyny pro nastavení fiskální integrace, aby mohli uživatelé provádět následující úlohy. 

- Konfigurovat fiskální konektory, které jsou fiskálními zařízeními nebo službami používanými pro účely fiskální registrace, jako je ukládání, digitální podpisy a zabezpečené odeslání fiskálních dat.
- Konfigurovat poskytovatele dokumentu, který definuje výstupní metodu a algoritmus generování fiskálního dokumentu.
- Konfigurovat proces fiskální registrace, který definuje postupnost kroků a skupinu konektorů použitých v každém kroku.
- Přiřadit procesy fiskální registrace do funkčních profilů POS.
- Přiřadit technické profily konektorů buď k hardwarovým profilům (pro místní fiskální konektory) nebo k funkčním profilům POS (pro jiné typy fiskálních konektorů).

## <a name="fiscal-integration-execution-flow"></a>Tok provádění fiskální integrace
Následující scénář zobrazí běžný tok provádění fiskální integrace.

1. Inicializace procesu fiskální registrace.
  
   Po provedení některých kroků, kdy je vyžadována fiskální registrace, například po uzavření maloobchodní transakce, je proces fiskální registrace přidružen k aktuálnímu funkčnímu profilu POS.

1. Vyhledávání fiskálního konektoru.
   
   Pro každý krok fiskální registrace zahrnutý v procesu fiskální registrace se systém spáruje se seznamem fiskálních konektorů. Tyto konektory mají funkční profil obsažený ve specifikované skupině konektorů se seznamem konektorů, které mají technický profil přidružený k aktuálnímu hardwarovému profilu (u typu konektoru, který se rovná pouze hodnotě **Místní**) nebo k aktuálnímu funkčnímu profilu POS (pro jiné typy konektorů).
   
1. Provedení fiskální integrace.

   Systém provede všechny potřebné akce definované sestavením propojeným s nalezeným konektorem. To se provádí v souladu s nastavením funkčního profilu a technického profilu, které byly pro tento konektor nalezeny v předchozím kroku.

## <a name="setup-needed-before-using-fiscal-integration"></a>Nastavení nutné před použitím fiskální integrace
Před použitím funkce fiskální integrace byste měli definovat následující nastavení:

- Definujte číselné řady na stránce **Parametry maloobchodu** pro číslo fiskálního funkčního profilu.
  
- Definujte číselné řady na stránce **Sdílené parametry maloobchodu** pro následující odkazy:
  
  - Číslo fiskálního technického profilu
  - Číslo skupiny fiskálních konektorů
  - Číslo procesu registrace

- Vytvořte **Fiskální konektor** v nastavení **Maloobchod > Nastavení kanálu> Fiskální integrace > Fiskální konektory** pro každé zařízení nebo službu, které chcete použít pro účely fiskální integrace.

-  Vytvořte **Poskytovatele fiskálního dokumentu** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Poskytovatelé fiskálních dokumentů** pro všechny fiskální konektory. Mapování dat je považováno za součást poskytovatele fiskálního dokumentu. Chcete-li nastavit různá mapování dat pro stejný konektor (například pravidla pro konkrétní stav), měli byste vytvořit různé poskytovatele fiskálních dokumentů.

- Vytvořte **Funkční profil konektoru** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Funkční profily konektoru** pro každého poskytovatele fiskálního dokumentu.
  - Zvolte název konektoru.
  - Vyberte poskytovatele dokumentu.
  - Určete nastavení sazeb DPH na kartě **Nastavení služby**.
  - Určete mapování kódů DPH a mapování typu úhrady na kartě **Mapování dat**.

  #### <a name="examples"></a>Příklad 

  |  | Formát | Příklad | 
  |--------|--------|--------|
  | Nastavení sazeb DPH | hodnota : VATrate | 1 : 2000, 2 : 1800 |
  | Mapování kódů DPH | VATcode : hodnota | vat20 : 1, vat18 : 2 |
  | Mapování typů úhrad | TenderTyp : hodnota | Hotovost : 1, Karta : 2 |

- Vytvořte **Skupiny fiskálních konektorů** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Skupina fiskálních konektorů**. Skupina konektoru je podmnožinou funkčních profilů propojených s fiskálními konektory, které provádí identické funkce a používají se ve stejné fázi v rámci procesu fiskální registrace.

   - Přidání funkčních profilů do skupiny konektoru. Klikněte na **Přidat** na stránce **Funkční profily** a vyberte číslo profilu.
   - Pokud chcete pozastavit použití funkčního profilu, nastavte **Zakázat** na **Ano**. 
   
     Tato změna ovlivní pouze aktuální skupinu konektoru. Můžete pokračovat s použitím stejného funkčního profilu v jiných skupinách konektoru.

     >[!NOTE]
     > Ve skupině konektoru může mít každý fiskální konektor pouze jeden funkční profil.

- Vytvořte **Technický profil konektoru** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Technické profily konektoru** pro každý fiskální konektor.
  - Zvolte název konektoru.
  - Zvolte typ konektoru: 
      - **Místní** – Nastavte tento typ pro fyzická zařízení nebo aplikace nainstalované v místním počítači.
      - **Interní** – Nastavte tento typ pro fiskální zařízení a služby připojené k serveru Retail Server.
      - **Externí** – Pro externí fiskální služby, jako je webový portál poskytovaný finančním úřadem.
    
  - Zadejte nastavení na kartě **Připojení**.

      
 >[!NOTE]
 > Aktualizovaná verze konfigurace, která byla načtena dříve, bude načtena pro technické i funkční profily. Je-li již použit vhodný konektor nebo poskytovatel dokumentů, budete upozorněni. Ve výchozím nastavení budou všechny změny provedené ručně ve funkčních a technických profilech uloženy. Chcete-li tyto profily přepsat pomocí výchozí sady parametrů z konfigurace, klikněte na tlačítko **Aktualizovat** na stránce **Funkční profily konektoru** a na stránce **Technické profily konektoru**.
 
- Vytvořite **Proces fiskální registrace** v nastavení **Maloobchod > Nastavení kanálu > Fiskální integrace > Procesy fiskální registrace** pro každý jedinečný proces fiskálních integrace. Registrační proces je definován sledem registračních kroků a skupinou konektorů používaných v každém kroku. 
  
  - Přidejte kroky registrace do procesu:
      - Klikněte na položku **Přidat**.
      - Zvolte typ konektoru.
      
      >[!NOTE]
      > Toto pole určuje, kde bude systém hledat konektor v technickém profilu, a to buď v hardwarovém profilu pro konektor typu **Místní**, nebo ve funkčních profilech pro jiné typy fiskálních konektorů.
      
   - Zvolte skupinu konektorů.
   
     >[!NOTE]
     > Klikněte na tlačítko **ověřit** pro kontrolu integrity struktury procesu registrace. Doporučujeme, aby ověření byla provedena v následujících případech:
       >- Pro nový proces registrace po dokončení všech nastavení, včetně vazby na funkční profily POS a hardwarové profily.
       >- Po provedení aktualizací existujícího procesu registrace.

-  Navázání procesů fiskální registrace na funkční profily POS v **Maloobchod > Nastavení kanálu > Nastavení POS > Profily POS > Funkční profily**.
   - Klikněte na tlačítko **Upravit** a vyberte **Číslo procesu** na kartě **Proces fiskální registrace**.
- Navažte technický profil konektoru na hardwarový profil v **Maloobchod > Nastavení kanálu > Nastavení POS > Profily POS > Hardwarové profily**.
   - Klikněte na tlačítko **Upravit** a potom klikněte na tlačítko **Nový** na kartě **Fiskální technický profil**.
   - Zvolte technický profil konektoru v poli **Číslo profilu**.
   
     >[!NOTE]
     > Můžete přidat několik technických profilů k hardwarovému profilu. To však není podporováno, pokud hardwarový profil má více než jeden průsečík s jakoukoliv skupinou konektoru. Abyste se vyhnuli nesprávnému nastavení, doporučujeme ověřit proces registrace po aktualizaci všech hardwarových profilů.

