platform :macos, '10.12'
use_frameworks!

target "Knuff" do
  pod 'Mantle', '2.1.6'
  pod 'KVOController'
  pod 'pop'
end

post_install do |installer|
  
  installer.pods_project.build_configurations.each do |config|
    config.build_settings['SDKROOT'] = 'macosx'
    config.build_settings['TARGETED_DEVICE_FAMILY'] = ''
    config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '$(inherited)'
    config.build_settings['TVOS_DEPLOYMENT_TARGET'] = ''
    config.build_settings['WATCHOS_DEPLOYMENT_TARGET'] = ''
  end
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SDKROOT'] = '$(inherited)'
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '$(inherited)'
      config.build_settings['TARGETED_DEVICE_FAMILY'] = '$(inherited)'
      config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '$(inherited)'
      config.build_settings['TVOS_DEPLOYMENT_TARGET'] = '$(inherited)'
      config.build_settings['WATCHOS_DEPLOYMENT_TARGET'] = '$(inherited)'
    end
  end
end
