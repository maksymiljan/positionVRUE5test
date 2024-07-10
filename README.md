@@ -0,0 +1,122 @@
#include "CoreMinimal.h"
#include "Misc/AutomationTest.h"
#include "MyVRGame/MyVRCharacter.h"

IMPLEMENT_SIMPLE_AUTOMATION_TEST(FVRCharacterHeadsetPositionTest, "MyVRGame.UnitTests.VRCharacterHeadsetPositionTest", EAutomationTestFlags::EditorContext | EAutomationTestFlags::EngineFilter)

bool FVRCharacterHeadsetPositionTest::RunTest(const FString& Parameters)
{
    // Create a VR character instance
    AMyVRCharacter* VRCharacter = NewObject<AMyVRCharacter>();

    // Simulate the initial position of the VR headset
    FVector InitialHeadsetPosition = FVector(0.0f, 0.0f, 180.0f);
    VRCharacter->SetHeadsetPosition(InitialHeadsetPosition);

    // Check if the headset position is set correctly
    TestEqual(TEXT("Headset Position should be set to the initial position"), VRCharacter->GetHeadsetPosition(), InitialHeadsetPosition);

    return true;
    #include "CoreMinimal.h"
#include "Misc/AutomationTest.h"
#include "MyVRGame/MyVRCharacter.h"

IMPLEMENT_SIMPLE_AUTOMATION_TEST(FVRCharacterHeadsetPositionTest, "MyVRGame.UnitTests.VRCharacterHeadsetPositionTest", EAutomationTestFlags::EditorContext | EAutomationTestFlags::EngineFilter)

bool FVRCharacterHeadsetPositionTest::RunTest(const FString& Parameters)
{
    // Create a VR character instance
    AMyVRCharacter* VRCharacter = NewObject<AMyVRCharacter>();

    // Simulate the initial position of the VR headset
    FVector InitialHeadsetPosition = FVector(0.0f, 0.0f, 180.0f);
    VRCharacter->SetHeadsetPosition(InitialHeadsetPosition);

    // Check if the headset position is set correctly
    TestEqual(TEXT("Headset Position should be set to the initial position"), VRCharacter->GetHeadsetPosition(), InitialHeadsetPosition);

    // Change the headset position
    FVector NewHeadsetPosition = FVector(10.0f, 20.0f, 200.0f);
    VRCharacter->SetHeadsetPosition(NewHeadsetPosition);

    // Verify the new headset position
    TestEqual(TEXT("Headset Position should be updated to the new position"), VRCharacter->GetHeadsetPosition(), NewHeadsetPosition);

    return true;
}
#pragma once

#include "CoreMinimal.h"
#include "Misc/AutomationTest.h"
#include "MyVRGame/MyVRCharacter.h"

class FVRCharacterHeadsetPositionTest : public FAutomationTestBase
{
public:
    FVRCharacterHeadsetPositionTest(const FString& InName, const bool bInComplexTask)
        : FAutomationTestBase(InName, bInComplexTask)
    {
    }

    virtual bool RunTest(const FString& Parameters) override;
};

IMPLEMENT_SIMPLE_AUTOMATION_TEST(FVRCharacterHeadsetPositionTest, "MyVRGame.UnitTests.VRCharacterHeadsetPositionTest", EAutomationTestFlags::EditorContext | EAutomationTestFlags::EngineFilter)
#include "VRCharacterHeadsetPositionTest.h"

bool FVRCharacterHeadsetPositionTest::RunTest(const FString& Parameters)
{
    // Create a VR character instance
    AMyVRCharacter* VRCharacter = NewObject<AMyVRCharacter>();

    // Simulate the initial position of the VR headset
    FVector InitialHeadsetPosition = FVector(0.0f, 0.0f, 180.0f);
    VRCharacter->SetHeadsetPosition(InitialHeadsetPosition);

    // Check if the headset position is set correctly
    TestEqual(TEXT("Headset Position should be set to the initial position"), VRCharacter->GetHeadsetPosition(), InitialHeadsetPosition);

    // Change the headset position
    FVector NewHeadsetPosition = FVector(10.0f, 20.0f, 200.0f);
    VRCharacter->SetHeadsetPosition(NewHeadsetPosition);

    // Verify the new headset position
    TestEqual(TEXT("Headset Position should be updated to the new position"), VRCharacter->GetHeadsetPosition(), NewHeadsetPosition);

    return true;
}
using UnrealBuildTool;

public class YourProject : ModuleRules
{
    public YourProject(ReadOnlyTargetRules Target) : base(Target)
    {
        PCHUsage = PCHUsageMode.UseExplicitOrSharedPCHs;

        PublicDependencyModuleNames.AddRange(new string[] { "Core", "CoreUObject", "Engine", "InputCore", "HeadMountedDisplay", "AutomationController" });

        PrivateDependencyModuleNames.AddRange(new string[] {  });

        // Uncomment if you are using Slate UI
        // PrivateDependencyModuleNames.AddRange(new string[] { "Slate", "Slate
using UnrealBuildTool;

public class YourProject : ModuleRules
{
    public YourProject(ReadOnlyTargetRules Target) : base(Target)
    {
        PCHUsage = PCHUsageMode.UseExplicitOrSharedPCHs;

        PublicDependencyModuleNames.AddRange(new string[] { "Core", "CoreUObject", "Engine", "InputCore", "HeadMountedDisplay", "AutomationController" });

        PrivateDependencyModuleNames.AddRange(new string[] {  });

        // Uncomment if you are using Slate UI
        // PrivateDependencyModuleNames.AddRange(new string[] { "Slate", "SlateCore" });

        // Uncomment if you are using online features
        // PrivateDependencyModuleNames.Add("OnlineSubsystem");

        // To include OnlineSubsystemSteam, add it to the plugins section in your uproject file with the Enabled attribute set to true
    }
}
