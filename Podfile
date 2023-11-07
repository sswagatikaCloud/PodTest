# Uncomment the next line to define a global platform for your project
 platform :ios, '14.0'

use_frameworks!


target 'PodTest' do
  # Comment the next line if you don't want to use dynamic frameworks

  # Pods for PodTest
  pod 'SwiftLint'
  
  target 'PodTestTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'PodTestUITests' do
    # Pods for testing
  end

end

post_install do |installer|
  set_minimum_deployment_target(installer)
end

def set_minimum_deployment_target(installer)
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |build_configuration|
      build_configuration.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '14.0'
    end
  end
end

def common_extension_target_pods
  pod 'SwiftLint'
  pod 'CenteredScrollView', '1.0.0'
end

target 'CallDirectoryExtension' do
  # Comment the next line if you don't want to use dynamic frameworks

  # Pods for CallDirectoryExtension
  common_extension_target_pods
end

target 'NotificationExtension' do
  # Comment the next line if you don't want to use dynamic frameworks

  # Pods for NotificationExtension
  common_extension_target_pods
end
