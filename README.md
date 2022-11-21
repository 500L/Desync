# Desync

G.Endo = true

game.RunService.Heartbeat:Connect(
    function()
        if _G.Endo then
            local CurrentVelocity = game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity

            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.Angles(0, math.rad(0), 0)

            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.Angles(0, math.rad(0.1), 0)
            game.Players.LocalPlayer.Character.HumanoidRootPart.AssemblyLinearVelocity =
                Vector3.new(math.random(3000), math.random(3000), math.random(3000))
            game.RunService.RenderStepped:Wait()
            game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = CurrentVelocity
        end
    end
